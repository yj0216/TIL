```
mysql -uroot -p;  
123456 
``` 
```  
create database opentutorials;  
use opentutorials;
```  
```  
create table topic(  
    id int(11) not null auto_increment,  
    title varchar(100) not null,  
    description TEXT null,  
    created datetime not null,  
    author varchar(30) null,  
    profile varchar(100) null,  
    primary key(id)  
); 
``` 


```
insert into topic (title,description,created,author,profile) values('MySQL','MySQL is ...',now(),'egoing','developer');  
insert into topic (title,description,created,author,profile) values('ORACLE','ORACLE is ...',NOW(),'egoing','developer');  
insert into topic (title,description,created,author,profile) values('SQL Server','SQL Server is ...',now(),'duru','data administrator');  
insert into topic (title,description,created,author,profile) values('PostgreSQL','PostgreSQL is ...',NOW(),'taeho','data scientist,developer');  
insert into topic (title,description,created,author,profile) values('MongoDB','MongoDB is ...',now(),'egoing','developer');  
```
```
+----+------------+-------------------+---------------------+--------+---------------------------+  
| id | title      | description       | created             | author | profile                   |  
+----+------------+-------------------+---------------------+--------+---------------------------+  
|  1 | MySQL      | MySQL is ...      | 2022-10-18 18:00:45 | egoing | developer                 |  
|  2 | ORACLE     | ORACLE is ...     | 2022-10-18 18:04:21 | egoing | developer                 |  
|  3 | SQL Server | SQL Server is ... | 2022-10-18 18:05:52 | duru   | data administrator        |  
|  5 | PostgreSQL | PostgreSQL is ... | 2022-10-18 18:13:01 | taeho  | data scientist, developer |  
|  6 | MongoDB    | MongoDB is ...    | 2022-10-18 18:14:03 | egoing | developer                 |  
+----+------------+-------------------+---------------------+--------+---------------------------+  
```
```
update topic set  description='Oracle is ...', title='Oracle' where id=2;  
rename table topic to topic_backup;  
```
```
create table topic(  
    id int(11) not null auto_increment,  
    title varchar(30) not null,  
    description text null,  
    created datetime not null,  
    author_id int(11) null,  
    primary key(id)  
);
```
```
create table author(  
    id int(11) not null auto_increment,  
    name varchar(20) not null,  
    profile varchar(200) null,  
    primary key(id)  
); 
```   
```
insert into author (id,name,profile) values(1,'egoing','developer');
insert into topic (id,title,description,created,author_id) values(1,'MySQL','MySQL is ...','2022-10-18 18:00:45',1);
insert into topic (id,title,description,created,author_id) values(2,'Oracle','Oracle is ...','2022-10-18 18:04:21',1);
insert into author (id,name,profile) values(2,'duru','database administractor');
insert into topic (id,title,description,created,author_id) values(3,'SQL Server','SQL Server is ...','2022-10-18 18:05:52',2);
insert into author (id,name,profile) values(3,'taeho','data scientist, developer');
insert into topic (id,title,description,created,author_id) values(4,'PostgreSQL','PostgreSQL Server is ...','2022-10-18 18:13:01',3);
insert into topic (id,title,description,created,author_id) values(5,'MongoDB','MongoDB is ...',' 2022-10-18 18:14:03',1);
```
```
select topic.id,title,description,created,name,profile from topic left join author on topic.author_id = author.id;

----+------------+-------------------+---------------------+--------+---------------------------+
| id | title      | description       | created             | name   | profile                   |
+----+------------+-------------------+---------------------+--------+---------------------------+
|  1 | MySQL      | MySQL is ...      | 2022-10-18 18:00:45 | egoing | developer                 |
|  2 | Oracle     | Oracle is ...     | 2022-10-18 18:04:21 | egoing | developer                 |
|  3 | SQL Server | SQL Server is ... | 2022-10-18 18:05:52 | duru   | data administractor       |
|  4 | PostgreSQL | PostgreSQL is ... | 2022-10-18 18:13:01 | taeho  | data scientist, developer |
|  5 | MongoDB    | MongoDB is ...    | 2022-10-18 18:14:03 | egoing | developer                 |
+----+------------+-------------------+---------------------+--------+---------------------------
```