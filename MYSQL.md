## MYSQL

>  open/close mysql in ubuntu：

```bash
service mysql stop
service mysql start
```

>  mysql log in  (  [ ] : optional parameters )
>
> + h  assign ip
> + P  assign port
> + u  assign user account
> + p  assign password

```bash
mysql [-h 127.0.0.1] [-P 3306] -u user account -p
```

## SQL setence

### overview:

#### grammar:

1. use one or more line as you like , end with ;
2. to make SQL setence readable,use **space** or **line breaks**
3. capital and small letter both worked , suggest to use capital letter for keyword

#### classify:

| classify | name                       | function                                       |
| -------- | -------------------------- | ---------------------------------------------- |
| DDL      | Data Definition Language   | define database object (database/table/fields) |
| DML      | Data Manipulation Language | CRUD (create/retrieve/update/delete)           |
| DQL      | Data Query Language        | find record in table,database                  |
| DCL      | Data Control Language      | create account , access control                |

#### comment in SQL setence:

single line:

```sql
--comment
#comment
```

multi line:

```sql
/*
comment
comment
*/
```

### DDL:

define database object (database/table/fields)

#### operate database:

1. search:

   + show all database

     ```sql
     SHOW DATABASES;
     ```

   + show recent database

     ```sql
     SELECT DATABASE();
     ```

2. create:

   + create database

     ```sql
     CREATE DATABASE[IF NOT EXISTS] database_name [DEFAULT CHARSET charset_name] [COLLATE range_rule];
     ```

     

3. delete 

   + delete database

     ```sql
     DROP DATABASE[IF EXISTS] database_name;
     ```

4. change

   + to operate a database,you need to use it first

     ```sql
     USE database_name;
     ```

     

#### operate table:



1. search all table in the database

   ```sql
   SHOW TABLES;
   ```

2. show table structure

   ```sql
   DESC table_name;
   ```


3. show create table(already exist) sentence

   ```sql
   SHOW CREATE TABLE;
   ```

4. create table 

   ```sql
   CREATE TABLE table_name( 
   id     int         comment "number",
   name   varchar(50) comment "name",
   age    int         comment "age",
   gender varchar(1)  comment "male/female"
   )comment "customer_info";
   ```

5. add field

   ```sql
   ALTER TABLE table_name ADD field_name type(length);
   ```

6. change field

   ```sql
   #change data type
   ALTER TABLE table_name MODIFY field_name type(length);
   #change field name and 
   ALTER TABLE table_name CHANGE old_field_name new_field_name type(length) comment"";
   ```

7. delete field

   ```sql
   ALTER TABLE tabLe_name DROP field_name;
   ```

8. rename table

   ```sql
   ALTER TABLE old_table_name RENAME TO new_table_name;
   ```

9. delete table

   ```sql
   #delete this table
   DROP TABLE [IF EXISTS] table_name;
   #delete table data
   TRUNCATE TABLE table_name;
   ```

   

### Data Type:

#### Var:

![](/home/liuchuan/Downloads/mdpicture/Screenshot from 2022-05-11 15-36-52.png)



for example , if you want to create an ==age== field , age cannot smaller than zero , so you can use UNSIGNED;

```sql
age TINYINT UNSIGNED comment "age"
```

#### Char:



<img src="/home/liuchuan/Downloads/mdpicture/Screenshot from 2022-05-11 15-44-46.png" style="zoom: 50%;" />

+ varchar & char:

  varchar & char(10) means text length is not allowed to beyond 10;

  > char(10) :
  >
  > if text length is not reach 10 , system will full the length to 10;
  >
  > **advantage: **performance better;
  >
  > varchar(10) :
  >
  > if text length is not reach 10 , system will keep the true length;
  >
  > **advantage**: use litter storage space;

#### Date:



<img src="/home/liuchuan/Downloads/mdpicture/Screenshot from 2022-05-11 15-56-28.png" style="zoom:67%;" />



usually use: DATE



#### Exercise:

<img src="/home/liuchuan/Downloads/mdpicture/Screenshot from 2022-05-11 16-00-15.png" style="zoom:33%;" />

```sql
CREATE TABLE staff( 
id    		  INT        		  comment "number",
jobNumber     VARCHAR(10)         comment "jobNumber",
name  		  VARCHAR(10)  		  comment "name",
gender		  VARCHAR(1)  		  comment "male/female",
age    		  TINYINT UNSIGNED    comment "age",
idNumber	  CHAR(18)            comment "ID number",
entryTime	  DATE				  comment "staff entry time"
)comment "staff_info";
```

### GUI software

use DataGrip(Jet Brains)



> database == Schema
>
> field == columns

+ **create database**

  right-click the connection->New->Schema->input new database name;

+ **create table**

  right-click the database->New->table->input new database name

  ->click "+" in columns to create fields

+ **modify table**

  right-click the table->modify table

> you can use console to input SQL sentence also
