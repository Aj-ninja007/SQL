# SQL
create database abc;
use abc;
create table employe(
id int primary key,
name varchar(1000),
mark int,
 grade char,
 city varchar(1000)
 );
 insert into employe (id,name,mark,grade,city)
 values
 (1,"anil",78,"c","puna"),
  (2,"amit",75,"b","mumbai"),
   (3,"ankur",98,"a","mumbai"),
    (4,"sandeep",66,"d","delhi"),
     (5,"sunil",74,"e","lko");



it select the all table 

      select *from employe  

it select only those city which have city name #

           select *from employe where city in("puna","delhi")
  it select distinct 

     select distinct city from employe

  limit is used to fixed data which you want to display means its give only 3 data
  
       select * from employe where mark >74 limit 3

  
  desc is used to arange decending order

  
    select * from employe order by mark desc

  asc  command is used to arrange in ascendind order 
  
      select * from employe order by mark asc



   group by jo hota vo group banadeta h jo bhi hum select krte h
   
    select city , count(id)
     from employe group by city 

# joins->is used to combine rows from two or more tables based on a related columns between them. #

TYPES OF JOINS
1->inner Join->dono tables k under common data hota h or common data ko lena ho to inner join use krte h
2->left->it is also called outer join,  do table h A TABLE and  B TABLE to ye  A table k sb data deta h or B Table me jo overlap kr rha h vo data dege
3->right->//
4->full-> dono table k combine information deta


##Inner Join
Return records that have matching values in both tables

syntax

           select columns(s)
           from tableA
           INNER JOIN tableB
           ON tableA.col_name=tableB.col_name;
     
