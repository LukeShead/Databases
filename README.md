# Databases

When designing software, databases are used all the time with them, this is because many websites will have the need to store information within it in order to make sure that the owners of the system can keep providing its customers the service that the database information will help provide. Databases give a way to let the users store information whilst allowing access to it by the owners, storing can be easy when it is done through databases as usually it is all done through tables that allow the information to be easily stored and easily viewed.

When creating a database, it is mostly done through tables, by creating and editing tables along with sorting them, data that is stored in databases are mostly done within tables that are split into different categories in order to allow the viewer of the database to see it's contents clearly.



When designing a database, it is usually the planning of how the database will function that will come first, for example a way of planning what a database will do is for an ERD diagram, this is the diagram that lets the developer and the viewer see how the database will operate and function. The ERD diagram will show the relationship between the tables within the database and can allow much easier development as the steps of the database can be looked at in better detail.

##### Below is the ERD of the database that I will create

This describes what all the tables will be called, what areas they will have within them and it will show how operates. It also shows which tables will interact with each other and in what way they will.

![ERD](https://github.com/LukeShead/Databases/blob/master/ERD%20for%20database.JPG)

As showed, the different tables are linked to each other, the "Heroes" table is linked to the "Heroes_Talents" table. This also follows the same rule with the "Enemies" table being connected to the "Enemies_Talents". What this means is that some people 



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

