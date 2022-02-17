

**The Entity-Relation diagram for the Carpooling database:**

Following is the description of Carpooling database

Carpooling database is based on the request from the user located in various cities who can choose the vehicle according to the vehicle identification and the ability of the people to share the vehicle. In the database, Employees must follow a route with a coordinated starting and ending point and within a time stamp.

The requirements are given below

**For each vehicle in the database, we should be able to see**

- The vehicle brand name
- The vehicle year name
- The maximum capacity of the vehicle
- The vehicle must have coordinates, and they must be unique.

**For each user in the database, we should be able to see**

- A user’s first name and last name.

**For each City in the database, we should be able to see**

- The city name
- The name of the state and country of the city.

**For each Employee in the database, we should be able to see.**

- An employee first name and last name
- An employee’s salary 
- Each employee must have a route for a carpooling request.
- An employee must be 18 years old or older.
- An employee must have a hiring date.

**For each Route in the database, we should be able to see**

- A route must have start and ending coordinates. 
- A route must have a start and ending timestamp.

**For each Carpooling Request in the database, we should be able to see**

- A carpooling request must have a date on which its created.

**Following are the tables or entities that are required to create a carpooling database:**

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

