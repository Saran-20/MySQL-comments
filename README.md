# MySQL-comments
### MySQL Create Database Statement
create database freshworks;
######Query OK, 1 row affected (0.02 sec)

### MySQL Show Databases Statement
show databases;

| Database           |
|:-----|
| book               |
| class              |
| freshworks         |
| information_schema |
| library            |
| mysql              |
| performance_schema |
| sys                |

###### 8 rows in set (0.02 sec)

### MySQL Use Database Statement
use freshworks;
######Database changed

### MySQL Create Table Statement
create table employees (id int primary key auto_increment,name varchar(20) not null,age int(2) not null,gender varchar(10) not null,salary int(5) not null);
######Query OK, 0 rows affected, 2 warnings (0.06 sec)

### MySQL Describe Table Statement
desc employees;

| Field  | Type        | Null | Key | Default | Extra          |
|:-----|:-----|:-----|:----|:----|:----|
| id     | int         | NO   | PRI | NULL    | auto_increment |
| name   | varchar(20) | NO   |     | NULL    |                |
| age    | int         | NO   |     | NULL    |                |
| gender | varchar(10) | NO   |     | NULL    |                |
| salary | int         | NO   |     | NULL    |                |

######5 rows in set (0.01 sec)

### MySQL Insert into Statement
insert into employees values (1,'saranya','18','female','5000'),(2,'jerusheya','18','female','5000'),(3,'abisha','18','female','5000'),(4,'swetha','18','female','5000'),(5,'haiden','19','male','10000'),(6,'aswath','18','male','10000'),(7,'rishi','19','male','10000'),(8,'annamalai','18','male','10000'),(9,'santhanu','20','male','10000'),(10,'riyas','18','male','10000'),(11,'selva','20','male','10000');
######Query OK, 10 rows affected (0.01 sec)
######Records: 10  Duplicates: 0  Warnings: 0

### MySQL Select Statement
select*from employees;

| id | name      | age | gender | salary |
|:-----|:----|:----|:----|:----|
|  1 | saranya   |  18 | female |   5000 |
|  2 | jerusheya |  18 | female |   5000 |
|  3 | abisha    |  18 | female |   5000 |
|  4 | swetha    |  18 | female |   5000 |
|  5 | haiden    |  19 | male   |  10000 |
|  6 | aswath    |  18 | male   |  10000 |
|  7 | rishi     |  19 | male   |  10000 |
|  8 | annamalai |  18 | male   |  10000 |
|  9 | santhanu  |  20 | male   |  10000 |
| 10 | riyas     |  18 | male   |  10000 |
| 11 | selva     |  20 | male   |  10000 |

######11 rows in set (0.00 sec)

### MySQL Where Statement
select * from employees where id='1';

| id | name    | age | gender | salary |
|:-----|:----|:----|:----|:----|
|  1 | saranya |  18 | female |   5000 |

######1 row in set (0.00 sec)

### MySQL Alter Table Statement
alter table employees add Email varchar(50);
######Query OK, 0 rows affected (0.03 sec)
######Records: 0  Duplicates: 0  Warnings: 0

select * from employees;

| id | name      | age | gender | salary | Email |
|:-----|:----|:----|:----|:----|:----|
|  1 | saranya   |  18 | female |   5000 | NULL  |
|  2 | jerusheya |  18 | female |   5000 | NULL  |
|  3 | abisha    |  18 | female |   5000 | NULL  |
|  4 | swetha    |  18 | female |   5000 | NULL  |
|  5 | haiden    |  19 | male   |  10000 | NULL  |
|  6 | aswath    |  18 | male   |  10000 | NULL  |
|  7 | rishi     |  19 | male   |  10000 | NULL  |
|  8 | annamalai |  18 | male   |  10000 | NULL  |
|  9 | santhanu  |  20 | male   |  10000 | NULL  |
| 10 | riyas     |  18 | male   |  10000 | NULL  |
| 11 | selva     |  20 | male   |  10000 | NULL  |

######11 rows in set (0.00 sec)

### MySQL Modify Statement
alter table employees modify Email varchar(30);
######Query OK, 11 rows affected (0.08 sec)
######Records: 11  Duplicates: 0  Warnings: 0

select *from employees;

| id | name      | age | gender | salary | Email |
|:-----|:----|:----|:----|:----|:----|
|  1 | saranya   |  18 | female |   5000 | NULL  |
|  2 | jerusheya |  18 | female |   5000 | NULL  |
|  3 | abisha    |  18 | female |   5000 | NULL  |
|  4 | swetha    |  18 | female |   5000 | NULL  |
|  5 | haiden    |  19 | male   |  10000 | NULL  |
|  6 | aswath    |  18 | male   |  10000 | NULL  |
|  7 | rishi     |  19 | male   |  10000 | NULL  |
|  8 | annamalai |  18 | male   |  10000 | NULL  |
|  9 | santhanu  |  20 | male   |  10000 | NULL  |
| 10 | riyas     |  18 | male   |  10000 | NULL  |
| 11 | selva     |  20 | male   |  10000 | NULL  |

######11 rows in set (0.00 sec)

### MySQL Update Statement
update employees set Email = "Saranya@gmail.com" where id=1;
######Query OK, 1 row affected (0.01 sec)
######Rows matched: 1  Changed: 1  Warnings: 0

select * from employees;

| id | name      | age | gender | salary | Email             |
|:-----|:----|:----|:-----|:----|:-----|
|  1 | saranya   |  18 | female |   5000 | Saranya@gmail.com |
|  2 | jerusheya |  18 | female |   5000 | NULL              |
|  3 | abisha    |  18 | female |   5000 | NULL              |
|  4 | swetha    |  18 | female |   5000 | NULL              |
|  5 | haiden    |  19 | male   |  10000 | NULL              |
|  6 | aswath    |  18 | male   |  10000 | NULL              |
|  7 | rishi     |  19 | male   |  10000 | NULL              |
|  8 | annamalai |  18 | male   |  10000 | NULL              |
|  9 | santhanu  |  20 | male   |  10000 | NULL              |
| 10 | riyas     |  18 | male   |  10000 | NULL              |
| 11 | selva     |  20 | male   |  10000 | NULL              |

######11 rows in set (0.00 sec)

### MySQL Delete Statement
######delete from employees where id=1;
######Query OK, 1 row affected (0.01 sec)

select * from employees;

| id | name      | age | gender | salary | Email |
|:-----|:----|:----|:----|:-----|:----|
|  2 | jerusheya |  18 | female |   5000 | NULL  |
|  3 | abisha    |  18 | female |   5000 | NULL  |
|  4 | swetha    |  18 | female |   5000 | NULL  |
|  5 | haiden    |  19 | male   |  10000 | NULL  |
|  6 | aswath    |  18 | male   |  10000 | NULL  |
|  7 | rishi     |  19 | male   |  10000 | NULL  |
|  8 | annamalai |  18 | male   |  10000 | NULL  |
|  9 | santhanu  |  20 | male   |  10000 | NULL  |
| 10 | riyas     |  18 | male   |  10000 | NULL  |
| 11 | selva     |  20 | male   |  10000 | NULL  |

######10 rows in set (0.00 sec)

### MySQL Drop Table Statement
drop table employees;
######Query OK, 0 rows affected (0.02 sec)

### MySQL Drop Database Statement
drop database freshworks;
######Query OK, 0 rows affected (0.03 sec)

show databases;

| Database           |
|:-----|
| book               |
| class              |
| information_schema |
| library            |
| mysql              |
| performance_schema |
| sys                |

######7 rows in set (0.00 sec)

##### CONSTRAINTS
### Not null
create table books (name varchar(30) not null);

### Unique
create table books (Email varchar (30) unique;

### Default
create table books (class varchar(20) default '12th');

### Check
create table books (age int (2) check (age>=18));

### Primary Key
create table books (id int(3) primary key auto_increnment);

### Create Table with Constraints without Foreign Key
create table students (id int(3) primary key auto_increment, name varchar(30) not null,Email varchar (30) unique,class varchar(20) default '12th',age int (2) check (age>=18));
######Query OK, 0 rows affected, 2 warnings (0.06 sec)

### Insert into
insert into students (name,Email,age) values ('saranya','Saranya@gmail.com','18');
######Query OK, 1 row affected (0.01 sec)

desc students;

| Field | Type        | Null | Key | Default | Extra          |
|:-----|:----|:----|:-----|:----|:----|
| id    | int         | NO   | PRI | NULL    | auto_increment |
| name  | varchar(30) | NO   |     | NULL    |                |
| Email | varchar(30) | YES  | UNI | NULL    |                |
| class | varchar(20) | YES  |     | 12th    |                |
| age   | int         | YES  |     | NULL    |                |

######5 rows in set (0.00 sec)


### Select 
select * from students;

| id | name    | Email             | class | age  |
|:-----|:----|:----|:----|:----|
|  1 | saranya | Saranya@gmail.com | 12th  |   18 |

######1 row in set (0.00 sec)

### Foreign Key
create table foreignkey(id int primary key auto_increment, mark int(2), foreign key(id) references students(id));
######Query OK, 0 rows affected, 1 warning (0.05 sec)

### Insert into
insert into foreignkey (mark,id) values ('98','1');
######Query OK, 1 row affected (0.01 sec)

desc foreignkey;

| Field | Type | Null | Key | Default | Extra          |
|:-----|:----|:----|:----|:----|:----|
| id    | int  | NO   | PRI | NULL    | auto_increment |
| mark  | int  | YES  |     | NULL    |                |

######2 rows in set (0.01 sec)

### Select
select * from foreignkey;

| id | mark |
|:-----|
|  1 |   98 |

######1 row in set (0.00 sec)

##### OPERATORS
### Select
select * from students;

| id | name    | Email             | class | age  |
|:-----|:----|:----|:----|:----|
|  1 | saranya | Saranya@gmail.com | 12th  |   18 |

######1 row in set (0.00 sec)

### And
select* from students where name='saranya' and age='18';

| id | name    | Email             | class | age  |
|:-----|:----|:-----|:----|:----|
|  1 | saranya | Saranya@gmail.com | 12th  |   18 |

######1 row in set (0.00 sec)

### Not 
select * from students where not age = 18;

| id | name      | Email          | class | age  |
|:-----|:----|:----|:----|:----|
|  2 | jerusheya | jeru@gmail.com | 12th  |   19 |
|  3 | abisha    | abi@gmail.com  | 12th  |   19 |

######2 rows in set (0.00 sec)

### Between
select * from students where age between 18 AND 20;

| id | name      | Email             | class | age  |
|:-----|:----|:----|:----|:----|
|  1 | saranya   | Saranya@gmail.com | 12th  |   18 |
|  2 | jerusheya | jeru@gmail.com    | 12th  |   19 |
|  3 | abisha    | abi@gmail.com     | 12th  |   19 |

######3 rows in set (0.00 sec)

### In
select * from students where age in (18);

| id | name    | Email             | class | age  |
|:-----|:----|:----|:----|:----|
|  1 | saranya | Saranya@gmail.com | 12th  |   18 |

######1 row in set (0.00 sec)

### Like
select * from students where name like 'ab%';

| id | name   | Email         | class | age  |
|:-----|:----|:----|:-----|:----|
|  3 | abisha | abi@gmail.com | 12th  |   19 |

######1 row in set (0.00 sec)

select * from students where name like '%ya';

| id | name      | Email             | class | age  |
|:-----|:----|:----|:----|:-----|
|  1 | saranya   | Saranya@gmail.com | 12th  |   18 |
|  2 | jerusheya | jeru@gmail.com    | 12th  |   19 |

######2 rows in set (0.00 sec)

### Any
create table marks(id int,mark int,name varchar(20));
######Query OK, 0 rows affected (0.05 sec)

insert into marks (id,mark,name) values (1,98,'saran'),(2,98,'jeru'),(3,98,'abi');
######Query OK, 3 rows affected (0.01 sec)
######Records: 3  Duplicates: 0  Warnings: 0

select * from marks;

| id   | mark | name  |
|:-----|:----|:----|
|    1 |   98 | saran |
|    2 |   98 | jeru  |
|    3 |   98 | abi   |

######3 rows in set (0.00 sec)

create table score(id int,mark int,name varchar(20));
######Query OK, 0 rows affected (0.04 sec)

insert into score (id,mark,name) values (1,98,'saranya'),(2,98,'jerusheya'),(3,98,'abisha');
######Query OK, 3 rows affected (0.01 sec)
######Records: 3  Duplicates: 0  Warnings: 0

select * from score;

| id   | mark | name      |
|:-----|:----|:----|
|    1 |   98 | saranya   |
|    2 |   98 | jerusheya |
|    3 |   98 | abisha    |

######3 rows in set (0.00 sec)

select mark from  marks where mark = any (select mark from score)

| mark |
|:-----|
|   98 |
|   98 |
|   98 |

######3 rows in set (0.00 sec)

##### AGGREGATE FUNCTIONS

select * from students;

| id | name      | Email             | class | age  |
|:-----|:----|:----|:----|:----|
|  1 | saranya   | Saranya@gmail.com | 12th  |   18 |
|  2 | jerusheya | jeru@gmail.com    | 12th  |   19 |
|  3 | abisha    | abi@gmail.com     | 12th  |   19 |

######3 rows in set (0.00 sec)

### Min
select min(age) from students;

| min(age) |
|:-----|
|       18 |

######1 row in set (0.00 sec)

### Max
select max(age) from students;

| max(age) |
|:-----|
|       19 |

######1 row in set (0.00 sec)

### Avg
select avg(age) from students;

| avg(age) |
|:-----|
|  18.6667 |

######1 row in set (0.00 sec)

### Count
select count(age) from students;

| count(age) |
|:-----|
|          3 |

######1 row in set (0.00 sec)

### Sum
select sum(age) from students;

| sum(age) |
|:-----|
|       56 |
######1 row in set (0.00 sec)

