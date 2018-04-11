# Databases

When designing software, databases are used all the time with them, this is because many websites will have the need to store information within it in order to make sure that the owners of the system can keep providing its customers the service that the database information will help provide. Databases give a way to let the users store information whilst allowing access to it by the owners, storing can be easy when it is done through databases as usually it is all done through tables that allow the information to be easily stored and easily viewed.

When creating a database, it is mostly done through tables, by creating and editing tables along with sorting them, data that is stored in databases are mostly done within tables that are split into different categories in order to allow the viewer of the database to see it's contents clearly.

When designing a database, it is usually the planning of how the database will function that will come first, for example a way of planning what a database will do is for an ERD diagram, this is the diagram that lets the developer and the viewer see how the database will operate and function. The ERD diagram will show the relationship between the tables within the database and can allow much easier development as the steps of the database can be looked at in better detail.

### Below is the ERD of the database that I will create

This describes what all the tables will be called, what areas they will have within them and it will show how operates. It also shows which tables will interact with each other and how that will affect the database

![ERD](https://github.com/LukeShead/Databases/blob/master/Final%20ERD.JPG) 

As showed, the different tables are linked to each other, the "Heroes" table is linked to the "Heroes_Talents" table. This also follows the same rule with the "Enemies" table being connected to the "Enemies_Talents". What this means is that only an entry to the Heroes table will be connected to an entry to the Heroes_Talents table and vise versa. However an enemy is not connected the Heroes table or the Heroes_Talents table but is connected to the Enemies_Talents table. All of these tables on link to one table however called "Skills", this table is connected to both the Talent tables and interacts with them both.

In the ERD it also shows the what the information within the tables are going to be, for example the Heroes table has ID, LEVEL, NAME, RACE and STATUS inside it. These areas will be able to have entries within the database that come under those areas, this will determine what data the database is storing and what each table will store in it.

### As well as an ERD, there are Data dictionaries

These are dictionaries which will help the viewer understand what type of input the table area will have, for example certain areas will have "text" next to them whereas others will have "float". This is to indecate whether there would be numbers or letters within the field of input. Data dictionaries are important as they can keep the database consistent from the start by giving it a set point as it allows viewers to look onto a clear view of what the database is going to be like and can always be referred back to when stuck.

![Data Dictionary](https://github.com/LukeShead/Databases/blob/master/Database%20spreadsheet.JPG)

In this data dictionary it shows how my database will be made and what value type they will have, by using this spreadsheet I will be able to always have a fixed layout of the database and how it will function. This will allow me to not get distracted with adding anything more or changing it within the development stage, with this I will be able to avoid any complications within my database

### User stories

When looking at the requirements for the database, it can all be summed up with the use of user stories, user stories are simple objectives that can be completed in order to cater for the user's or clients needs and can be used as bookmarks in objectives and aims when completing a project.

User stories of this project:

- I would like to be able to see how much HP my hero has.
- I would like to be able to how much HP the enemies have.
- I would like to be able to track my heroes level.
- I would like to be able to track the enemies level.
- I would like to be able to see what skills I have.
- I would like to be able to see what skills enemies have.
- I would like to be able to check the status of my hero.
- I would like to be able to check the status of my enemies.
- I would like to be able to read the names of my heroes.
- I would like to be able to read the names of my enemies.
- I would like to be able to see the race of my heroes.
- I would like to be able to see the race of the enemies.
- I would like to be able to see how much damage a skill does.
- I would like to be able to see how much healing a skill does.
- I would like to be able to see the type of skill that my hero has.
- I would like to be able to see the type of skill that my enemies have.

These user stories were used in order to help plan the database and when developing it, allowed clear objectives.

## Developing the database

When developing the database, I used SQL in order to insert tables, update them with any information, select different fields from tables and link tables.

With this I used different commands in order to accomplish this, some of the commands I used with SQL are:

### Insert

This is for filling out empty table and adding values to them, by doing this the database can have values to store and edit. This command is needed to add values using the query language.

### Update

This is the command that updates the values that are in the fields within their respected tables, this is used when certian values in certain fields need to be changed and does not require the whole table to be changed with it. This can be very useful when needing to quickly change a value in many situations.

### Select and Where

These two commands are put into the same catagory as they both do similar things, the select command will select a table, field or values in order for them to be edited, for example a select command and update can be ran at the same time in order to edit a certain part of the database and not all of it. 

Where is similar in which it can be used with commands like update in order to complete its task, for example where there might be certain values, means that all values that come under the where command can be edited in any way, whereas select is more broad, whereas is very direct with its selecting.

### Delete

This is the command that is used in order to delete a value to a table's worth of data, it is used when data is no longer being used or needs to be removed from the database for situational reasons.

## Code I used in order to build the database

CREATE TABLE HEROES( ID INT NOT NULL PRIMARY KEY, LEVEL INT NOT NULL, NAME VARCHAR(100) NOT NULL, DAMAGE FLOAT NOT NULL, RACE NOT NULL, STATUS NOT NULL, HP FLOAT NOT NULL, DAMAGE NOT NULL, );

CREATE TABLE HEROES_SKILLS( SKILL_ID INT NOT NULL PRIMARY KEY, RANK INT NOT NULL PRIMARY KEY, DAMAGE/HEAL INT NOT NULL, );

CREATE TABLE ENEMIES( ID INT NOT NULL PRIMARY KEY, NAME VARCHAR(100) NOT NULL, HP FLOAT NOT NULL, DAMAGE FLOAT NOT NULL, );

CREATE TABLE ENEMIES_SKILLS( ENEMY_ID INT NOT NULL PRIMARY KEY, SKILL_ID INT NOT NULL PRIMARY KEY, RANK INT NOT NULL, DAMAGE/HEAL INT NOT NULL, );

CREATE TABLE SKILLS( ID INT NOT NULL PRIMARY KEY, TYPE INT NOT NULL, NAME VARCHAR(100) NOT NULL, RANGE INT NOT NULL, );

### Code I used.

INSERT HEROES
SET LEVEL, NAME, HP, STATUS = 1

UPDATE HEROES
SET LEVEL = 4, HP=200
WHERE NAME LIKE 'Dem Bois%';

SELECT * FROM HEROES;

WHERE NAME LIKE 'Dem Bois%';

SELECT H.NAME, H.LEVEL,
S,NAME, HS.LEVEL

FROM HEROES H, SKILLS S,
HEROES_SKILLS HS

WHERE HEROES_ID = H.ID AND
SKILL_ID = S.ID AND NAME LIKE '%a%' 

SELECT COUNT (*) FROM HEROES;

SELECT MAX(H.LEVEL), MIN(H.LEVEL)
FROM HEROES H;

## The User Manual

User and Technical Manual

Table of Content

1.0 General Information
1.1 System Overview
1.2 The Role of Database Systems As...
1.2.1 Back-end Systems
1.2.2 E-Commerce
1.2.3 Data Mining Applications
1.3 Tools Used

2.0 System Summary
2.1 What Is An Object Oriented Database?
2.2 What Is The System For?






1.0 General Information


1.1 System Overview

This database system is designed to hold information on different characters that appear in the game. It has different tables for Heroes, Enemies and other tables relating to skills that hold all of the key values relating to that character, including Name, ID, Health and Damage. These values can be updated in real time for gameplay purposes.

1.2 The Role Of Database Systems As…

Database systems can be used for a wide variety of things. The following is a list of different uses of database systems and what purpose they serve.

	1.2.1 Back-end Systems
	
A Back-End Database is a database that can be accessed by different users through a third-party application rather than by application programming stored within the database itself or by manipulation of the data.
	
1.2.2 E-Commerce

In E-commerce, the main purpose of a database is to store information about the customer transactions, customer care, and inventory. By using a database,  programming a dynamic E-commerce website becomes easy as you only focus on the presentation and behavior of the website while all interactions are being managed by the system.

	1.2.3 Data Mining Applications

Data mining is the process of discovering patterns in large data sets using different methods. It is an essential process where intelligent methods are applied to extract data patterns. During the process of data mining, the database(s) are searched for key information that could uncover new patterns or sequences in the data.


1.3 Tools Used

The following tools were used in the design and creation of the database system:

	-  draw.io 
	Used to create the Entity Relationship Diagram

	-  Microsoft Excel
	Used to create the data dictionary and the test plan documentation

	-  Microsoft Access
	Used to create the database system

 	-  Microsoft Word
	Used to create the user and technical documentation











2.0 System Summary


2.1 What Is An Object Oriented Database?

An object database is a database system in which data is represented in the form of objects similar in design to object oriented programming. Object databases are different from relational database which are table-oriented. Object-relational databases are a mix of both approaches. 

Object-oriented database management systems combine database capabilities with object oriented programming language capabilities. This design allows object-oriented programmers to develop the product, store them as objects, and duplicate and edit existing objects to make new objects Because the database is connected with the programming language, the programmer can maintain a high level of consistency, in that both the OODBMS and the programming language will use the same model to represent themselves. Relational database management system projects maintain a clearer division between the database model and the application.

2.2 What Is The System For?

The system is designed to hold data on the status of different characters and spells within the game, this system will help the game be able to hold multiple bits of data in order to complete it's task.


### The Database.

![The Database](https://github.com/LukeShead/Databases/blob/master/Database.JPG)

This is the database that contains all the data that is needed to be stored.


### Test plan 

![Test Plan](https://github.com/LukeShead/Databases/blob/master/Test%20plan.JPG)

This test plan was to test different elements of the database in order to make sure that all elements of the database worked after it was completed.

## Evidence screenshots

![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%201.JPG)
![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%202.JPG)
![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%203.JPG)
![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%204.JPG)
![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%205.JPG)
![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%206.JPG)
![](https://github.com/LukeShead/Databases/blob/master/test%20plan%20evi%207.JPG)
![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%208.JPG)
![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%209.JPG)
![](https://github.com/LukeShead/Databases/blob/master/Test%20plan%20evi%2010.JPG)
![](https://github.com/LukeShead/Databases/blob/master/test%20plan%20evi%2011.JPG)

These screenshots are all parts of my database and show how the database looked and outputted information, as well as this it was able to update when told too.
