# crud-node-mysql
Basic CRUD operations using MySql

### Packages:
express-validator: 
	This module used for form validation.

body-parser: 
	This module is used to read HTTP POST data. It’s an express middleware that reads form’s input and store it as javascript object.

method-override: 
	This module let us use HTTP verbs such as PUT or DELETE in places where they are not supported. This module provides different ways of overriding like overriding using header, overriding using query value, or through custom logic. In this CRUD application, we will be using the custom logic of overriding.

express-flash: 
	Flash messages are shown for some time and cleared after being displayed to the user. They are mainly used when we have to redirect to next page and show certain message like success message or error message. Flash messages are store in session.

cookie-parser & express-session modules:
	Flash messages are stored in session. So, we also have to install and use cookie-parser & session modules.

EJS:
	EJS is packaged with view helpers. View helpers are shortcuts to commonly used display code, like links and forms.

mysql:
	To access a MySQL database with Node.js, you need a MySQL driver.

express-myconnection:
	Express middleware to provide consistent API for MySQL connection. It can auto close/release mysql connection. Using this module, the connection can be accessed anywhere in router.


### Get clone and install npm
```
	crud-node-mysql>npm install
```

### MySql
Create a database named node_test_db 
Create users table
```
	CREATE TABLE users (
		id int(11) NOT NULL auto_increment,
		name varchar(100) NOT NULL,
		age int(3) NOT NULL,
		email varchar(100) NOT NULL,
		PRIMARY KEY (id)
	);
```
config.js : This file basically contains your database credentials.

app.js : We load all the modules that we installed in above steps.

routes/users.js: This file is responsible for handling CRUD operations like adding, editing, deleting and viewing users from database. Database queries, form validation and template rendering is done here.