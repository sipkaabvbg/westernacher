# Westernacher CRUD Application 
The Westernacher CRUD Application is web application that manages user accounts in a database. 
The application has the following functionality:
1. A list page that shows all user accounts in a sortable grid.
2. Create new account dialog that adds new accounts to the database. 
The following properties should be supported
	First name
	Last name
	Email address
	Date of birth
3. A Delete account dialog that removes accounts from the database.
4. An Edit account dialog that allows to change account data of existing accounts.

Restrictions: users with the same names and dates of birth can be registered in the application because 
it is possible to exist people with coincident names or dates of birth.
The email address field is unique for each user and can not register users with the same email address.

## Build and Run

Project should be build and run using Java 1.8, after it has been added to Eclipse IDE.

1. To run the application you must initially start MySQL database and create a schema whit name "westernacher"

2. Open the "application.yml" file and set your own configurations for the
       database connection.
    
3. Build with Maven "mvn clean install"  
    
4. Change directory to "../WesternacherCRUD/target/"
     
5. Execute in the terminal "java -jar crud.user-1.0.0.jar" 
    
Alternatively run "mvn spring-boot:run" from command line or IDE or execute "com.westernacher.crud.WesternacherCRUD.main()" from within IDE.
 
After a successful start of the application, a graphical interface can be opened in a browser on:
http://localhost:8080/westernacher

The birthday field is activated by placing the cursor on the right side of the text box.

## Used technology
Spring Boot, AngularJS, CSS Bootstrap, Spring Data, JPA/Hibernate and MySQL

## Design
### API Backend
The project contains an API package "com.westernacher.crud.api" with all the interfaces describing the main application functionality.
### Implementation Backend

The implementation of functionality is found in the following packages:
-com.westernacher.crud -this package is the primary launch class of the application
-com.westernacher.crud.controller -this package contains the controllers in the application
-com.westernacher.crud.configuration -this package contains the configuration class
-com.westernacher.crud.model -this package keeps the class describing the application domain
-com.westernacher.crud.service -this package contains service class for all user-related operations
-com.westernacher.crud.util -this package contains helper class to send errors

### Front-end
The Freemarker templates are used for views.
Controllers are written on AngularJs and they are UserRegistrationService.js and UserRegistrationController.js

