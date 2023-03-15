# DATABASE  
스프레드시스템과 비슷한 구조인 표 형식으로 되있으나    
스프레드 시스템이 클릭을 통해 데이터를 제어하는것과 다르게  
데이터베이스는 컴퓨터 언어를 통해 제어할 수 있음

데이터 저장 -> 표(table)  
table 그루핑 -> 데이터베이스(스키마)  
스키마 그루핑 -> 데이터베이스 서버  
  
보안 -> 자체적인 보안 체계를 통해 안전하게 데이터를 보관함  
권한 -> 여러 사람이 사용가능하고 사람마다 차등적으로 권한을 줄 수 있음    
## 관계형 DATABASE  
중복을 줄여주고 DATABASE 유지보수가 훨씬 편해짐  
     
# SQL 
Structured Query Language(구조화된 데이터베이스 언어)  
특징 -> 쉬움,중요함    
CRUD -> *Create *Read Update Delete  

# 데이터베이스 명령어  
create database '이름' -> 데이터베이스 생성  
drop database '이름' -> 데이터베이스 삭제  
show databases -> 데이터베이스 열람  
use '이름' -> 사용할 데이터베이스 선택    
primary key(column) -> table에서 고유한 값을 가지도록 설정  
create table '이름'(값) -> table 생성  
show tables -> table 열람   
desc 'table' -> talbe 구조 열람  
insert into '이름' ('column') values('row') -> table 행(row) 삽입(column과 values에 순서는 같아야함)  
select * from 'table' -> talbe 모든 내용 열람    
select 'column' from 'table' -> table 'column' 내용만 열람  
update 'table' set 'column='바꾸고 싶은 내용'' where 'column='바꾸싶은 곳의 row'' -> table 내용을 바꿈   
delete from 'table' where 'column='바꾸싶은 곳의 row'' -> table 행을 삭제 시킴  
 select *('column') from 'table' left join 'table' on 'table'.'column' = 'table'.'column' -> 두개의 table을 하나로 합침  
 