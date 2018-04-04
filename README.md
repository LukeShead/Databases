# Databases

When designing software, databases are used all the time with them, this is because many websites will have the need to store information within it in order to make sure that the owners of the system can keep providing its customers the service that the database information will help provide. Databases give a way to let the users store information whilst allowing access to it by the owners, storing can be easy when it is done through databases as usually it is all done through tables that allow the information to be easily stored and easily viewed.

When creating a database, it is mostly done through tables, by creating and editing tables along with sorting them, data that is stored in databases are mostly done within tables that are split into different categories in order to allow the viewer of the database to see it's contents clearly.









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

