# MySQL Import and Export Tutorial

MySQL is an open-source relational database management system (RDBMS) that ranks as the second most popular database in the world. It offers a rich set of features, allowing you to start with small databases and scale according to your requirements. MySQL also supports server replication for load balancing. This tutorial will guide you through the process of importing and exporting MySQL databases using the command-line interface.

## Exporting MySQL Databases Using Command Line

MySQL provides a utility called `mysqldump` to export databases. This tool is easy to use and allows you to export a single database or multiple databases.

### Export a Single Database

To export a single database using `mysqldump`, connect to your server via SSH and execute the following command:

```bash
$ mysqldump -uUSERNAME -p DB_NAME > exported.sql

Importing MySQL Databases Using Command Line
Importing a MySQL database is straightforward with the mysql command. Before you can import, you'll need to create a database in MySQL where the data will be imported.

Create a New MySQL Database
Log in to your MySQL server:

bash
Copy code
$ mysql -uUSERNAME -p
After logging in, create a new database:

sql
Copy code
mysql> CREATE DATABASE DB_NAME;
Replace DB_NAME with the name you want to give to your new database.
Import the SQL File into the Database
Once the database is created, you can import your SQL file into this database using the following command:

bash
Copy code
$ mysql -uUSERNAME -p DB_NAME < imported.sql
Replace USERNAME with your MySQL username.
Replace DB_NAME with the name of the database you just created.
Replace imported.sql with the name of the SQL file you wish to import.
You will be prompted to enter your password. After authentication, the import process will begin, and the data from imported.sql will be loaded into the specified database.
