# data-engineering-learning
Here I gathered all information and knowledge for data engineering..
## For the Data Engineering Base:
### 1. Knowledge on SQL and NoSQL databases
- Relational databases
	- Oracle Database
	- MySQL Database
	- PostgreSQL Database
		- Downloaded and completed the setup postgresql 15.1.1
			- Link: https://www.enterprisedb.com/downloads/postgres-postgresql-downloads
		- Shell SQL(psql)
			- Check database details:\d
			- Check specific database tables details with sequence: \dt
			- Check specific database tables details: \t
			- To on the expand  shell display for big table(horizontally):\x
			- To on the expand  shell display:\x  
			- Creating database and perform CRUD operation
				- CREATE DATABASE test;
				- CREATE TABLE person(
				 id BIGSERIAL NOT NULL PRIMARY KEY,
				 name VARCHAR(100) NOT NULL,
				 country VARCHAR(50) NOT NULL);
				- \d: check test database table details
				- \dt
				- select * form person;
				- Inserting data into the table:
					- insert into person (name, country) values('Pankaj', 'BD');
					- insert into person (name, country) values('Chanchal', 'USA');
					- insert into person (name, country) values('Anup', 'GE');
					- insert into person (name, country) values('Bibhuti', 'BD');
					- insert into person (name, country) values('Shaishab', 'BD');
					- insert into person (name, country) values('Subir', 'BD');
					- insert into person (name, country) values('Mithu', 'BD');
					- insert into person (name, country) values('Sanaton', 'USA');
					- select * from person where name like 'Pan%';
					- select * from person where name like '%an%;
					- select * from person;
					- select count(id) from person;
					- select count(id) from person;
					- update person set name = 'Chanchal' where id = 8;
					- select * from person;
					- delete from person where id = 7;
- Non Relational Databases

### 2. SQL

### 3. Python/Scala
A programming language and some sort of programming knowledge.

### 4. Data Pipeline/ Data Warehousing
#### SNOWFLAKE DATA WAREHOUSE:
- Difference between Authetication and Authorization:
  - Authentication is to authenticate a user. As a example authenticate by user name and password.
  - Authorization is the give permission for use or something to do
- Difference between Identity and Access:
  - Identity is referred as combination of someones name(username), address, nationality, etc.
    - Passing an identity check is called Authentication.
    - Identity is about WHO you are.
    - Identity is sometimes tested proven through username and password  combinations.
  - Accsss is referred as what is allowed to do or use something.
    - Proving  right to access something is called Authorization
    - Access is about WHAT you can see/do.
    - Access is sometimes tested and awarded through RBAC(Role Based Access Control) role assignments.
- Difference between User and Role:
  - User is a person who will be assigned the roles to do or control
  - Roles are assigned to the User. User can switch between the different roles.
- Roles are in snowflake:
  - ACCOUNTADMIN
  - SYSADMIN 
  - SECURITYADMIN
  - USERADMIN
  - PUBLIC
- Here the most powerfull role is ACCOUNTADMIN.
- SYSADMIN and SECURITYADMIN is under ACCOUNTADMIN
- A data created by ACCOUNTADMIN is the only owner of this data base. But if  ACCOUNTADMIN role transfer the ownwership to SYSADMIN then SYSADNIN will also have the ownership of that database. 
- Every data base created in snowflake will have two schema
  - INFORMATION_SCHEMA
     - Not changeable: cration table, delete table, ....
  - PUBLIC 
     - Changeable: cration table, delete table, ....
- If the ownership is tranfered the the INFORMATION_SCHEMA is also transfered but not the PUBLIC schema. It need to be manually shared. 
- Using WORKSHEETS:
  - writing some SQL code
    	- SELECT 'HELLO';
	- SELECT 'HELLO' AS "GREETINGS";
	- SHOW DATABASES;
	- SHOW SCHEMAS IN ACCOUNT;
	- CREATE OR REPLACE TABLE ROOT_DEPTH(
    ROOT_DEPTH_ID NUMBER(1),
    ROOT_DEPTH_CADE TEXT(1),
    ROOT_DEPTH_NAME TEXT(7),
    UNIT_OF_MEASURE TEXT(2),
    RANGE_MIN NUMBER(2),
    RANGE_MAX NUMBER(2)
    );
    
	- alter table GARDEN_PLANTS.VEGGIES.ROOT_DEPTH 
	- RENAME COLUMN ROOT_DEPTH_CADE TO ROOT_DEPTH_CODE;
	- USE WAREHOUSE COMPUTE_WH;

	- INSERT INTO ROOT_DEPTH (
	ROOT_DEPTH_ID ,
	ROOT_DEPTH_CODE ,
	ROOT_DEPTH_NAME ,
	UNIT_OF_MEASURE ,
	RANGE_MIN ,
	RANGE_MAX 
)

	- VALUES
(
    1,
    'S',
    'Shallow',
    'cm',
    30,
    45
)
;

	- SELECT * FROM ROOT_DEPTH
limit 1;

	- INSERT INTO ROOT_DEPTH (
	ROOT_DEPTH_ID ,
	ROOT_DEPTH_CODE ,
	ROOT_DEPTH_NAME ,
	UNIT_OF_MEASURE ,
	RANGE_MIN ,
	RANGE_MAX 
)

	- VALUES
(
    2,
    'M',
    'Medium',
    'cm',
    45,
    60
)
;


	- INSERT INTO ROOT_DEPTH (
	ROOT_DEPTH_ID ,
	ROOT_DEPTH_CODE ,
	ROOT_DEPTH_NAME ,
	UNIT_OF_MEASURE ,
	RANGE_MIN ,
	RANGE_MAX 
)

	- VALUES
(
    3,
    'D',
    'Deep',
    'cm',
    60,
    90
)
;

	- select * From ROOT_DEPTH;
	
- Inserting data or uploading data to database:
	- uploading CSV files
### 5. Knowledge on Cloud Databases

### 6. A Data Engineering project
