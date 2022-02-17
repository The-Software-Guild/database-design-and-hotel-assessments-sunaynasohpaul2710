

The Entity-Relation diagram for the Carpooling database:

Following is the description of Carpooling database

Carpooling database is based on the request from the user located in various cities who can choose the vehicle according to the vehicle identification and the ability of the people to share the vehicle. In the database, Employees must follow a route with a coordinated starting and ending point and within a time stamp.

The requirements are given below

1. A route must have start and ending coordinates. 
1. A vehicle must have coordinates, and they must be unique.
1. An employee must have a hiring date.
1. An employee must be 18 years old or older.
1. Each table has its primary key
1. One vehicle must have only one carpooling request.
1. Each employee must have a route for a carpooling request.
1. Employee may have one or more vehicles.

Following are the tables or entities that are required to create a carpooling database


**USER** 

User\_Id INT ( PK)

Vehicle\_Id INT (FK)

user\_firstname VARCHAR(100)

user\_lastname VARCHAR(100)

**VEHICLE**

vehicle\_Id INT (PK)

request\_id INT (FK)

route\_id INT (FK)

brand VARCHAR(100)

year YEAR

max\_capacity\_Inkilos  INT

coordinates  POINT U

**EMPLOYEE**

employee\_id INT (PK)

user\_id INT (FK)

emp\_firstname VARCHAR(100)

emp\_lastname VARCHAR(100) 

emp\_salary INT

emp\_age INT

date\_fired DATE

date\_hired DATE

**ROUTE**

route\_Id INT (PK)

ciity\_Id INT (FK)

timestamp\_start TIMESTAMP

timestamp\_end TIMESTAMP

coordinate\_start POINT

coordinate\_END POINT


**CITY**

city\_id INT (PK)

city\_name VARCHAR(100)

state VARCHAR(100)

country VARCHAR(100)

**CARPOOLINGREQUEST**

request\_id INT (PK)

user\_Id  INT (FK)

created On DATE

**CITY\_CARPOOLINGREQUEST**

City\_Id INT (PK,FK)

Request\_ID Int (PK,FK)

![](Aspose.Words.998a5700-b4b0-4ef0-8e2b-56c1ba17f296.001.jpeg)
