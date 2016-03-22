###1) Use Proper package structure
Don't keep all type of code files into same folder. Create different packages to logically separate codes and put them into their respective places.
For example, all configuration related codes should go into configuration package, all database connection related code should go into persistent.
You can be creative about naming packages. The package naming stands follow like com.CompanyName.namespace1 or org.OrganizationName.namespace1.
 
###2) Use Configuration file for Variable parameters
Always remember to create conf file for changeable parameters used in code. Something like database name or Server IP address.
 
###3) Use proper name for variable
Avoid using random variable name. You are allowed to choose variable with long name but it should be representable of what is is or what it is storing.
Don't use q for query and i for looping.
 
###4) Use import statement properly
Many people use * to import everything from some package or library while using only one or two class/method from it. 
There are two problems with this practice, first is you are importing unwanted code and second that you can not backtrack which class/method came from which library.
write import statement for each method/class you use although they are from same package
 
###5) Use absolute import
Sometimes the user defined classes/libraries are available in classpath/pythonpath. You can import them as follow: import myclass. Don't do that.
Always write full import package name. like com.mycompany.xxx.myclass

###6) Close Database connection
While working with database, we open connection, we perfrom operations but we don't close connection. This is ill practice. 
Most of the database has limitation on number of concurrent open connections. It is more likely that in production environment, this limit is reached and all future connections are refused.
Database connection have timeout for dropping connection when they are not closed in your code. 
Until than your connection remains open and once it reach to predefined/default concurrent connection count, other user get connection refused error.  

###7) Limit Number of Database connection
Database connection opening and closing is time consuming affair. 
So let say you have 1 Lakh record to insert in database and if you open and close connection for each record that it will take lot of time.
Always try to reuse already opened connection handler and whenever bulk record insertion is required, use bulk insert query statements.


###8) Use code conventions
Most of the programing language has standard code conventions. Which give direction for writing code in standard format.
For java: http://www.oracle.com/technetwork/java/codeconvtoc-136057.html
For python: PEP 0008, pyflakes
Follow them for all you coding practices