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

  #QUESTION
  
ques 1->Show first name of patients that start with the letter 'C'

        SELECT first_name FROM patients where first_name like "C%"

  ques2->Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)

        SELECT first_name FROM patients where weight between 100 and 120

  ques3->Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA'

        update patients
        set allergies='NKA'
        where allergies is Null


   ques->Show first name and last name concatinated into one column to show their full name.

          select CONCAT(first_name ,  ' ' ,last_name)  from 
              patients

 ques5->  Show first name, last name, and the full province name of each patient.

Example: 'Ontario' instead of 'ON'


            select first_name,last_name,province_name from patients as p 
      join province_names as pn on
     p.province_id = pn.province_id;



ques 6->Show how many patients have a birth_date with 2010 as the birth year.

        select count(patient_id)from patients where year(birth_date)=2010

