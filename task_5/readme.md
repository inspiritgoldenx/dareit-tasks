# task 5
## the main goal of the task was to learn how to create Cloud SQL instance 😺
1. first of all I opened **Cloud SQL** from the *Navigation Menu* in Google Cloud and clicked ***CREATE INSTANCE***
2. after that, I chose the **PostgreSQL** (second option) and filled the information there
3. I have added: Instance ID = *dareit-pg* (because the instance-id needs to be unique within the GCP project), Password = *whatever* (I made some up), Database version = here I chose *PostgreSQL 14* because that is the version of the engine, configuration to start = I chose *Sandbox* (because it's for me to train)
4. next step was to customize the instance, so I went to *Connections* where I chose **Public IP** , then I chose **ADD NETWORK** (under the Authorised Networks section) - thanks to that, I will be able to add an IP from which packets will be allowed to the Database Instance
5. so after that, I have googled my IP number and pasted it into *Newtork* field, then **save** and the instance was created 
![dareITsql](https://user-images.githubusercontent.com/125319277/231809830-c437555a-1997-4b71-abc1-0072f7661135.jpg)
6. the second step in the task was to use a program named *Dbeaver* to connect to the database 
7. after opening Open Dbeaver, on the left hand side in the white space - I clicked with the right click and chose to *Create New Folder*, I named it **DareIT**
8. then by clicking the folder and chose **Create Connection** --> and chose **PostgreSQL** 
9. after opening it, I had to fill the new opened window with some data: host = here I entered *my IP address*, Database = *postgres*, Port = *5432* (I think it was already set by default), Username = *postgres* (also set by deafult), Password - here I typed the same passwort, which I had provided for the admin user while creating the instance.
10. after everything was added, tried to test the connection and 🎉 it worked!
11. next step in the task was to create a schema in the database, so I clicked on the **Schemas** --> **create new schema** and typed the name of the schema
12. afterwards, I clicked with the right click on the new generated folder which appeard in *Schemas* --> *dareit* and chose **new sql script**
13. a new editor showed up, where I pasted this SQL code:
  ```
  CREATE TABLE students (

    id int,

    lastName varchar(255),

    firstName varchar(255),

    email varchar(255),

    city varchar(255)

);
```
14. to execute it, I clicked the orange arrow on the left and thanks to that, I received newly created Table in the Navigator
15. after this I chose Generate SQL by clicking with the right click and saw few commands which I can use, for example *INSERT* --> it generated for me a code, which I can later edit, the code looked:
```
INSERT INTO dareit.students

(id, lastname, firstname, email, city)

VALUES(0, '', '', '', '');
```
16. after generating the code, I filled it up with some data (as above: id, lastname etc.)
17. later I selected data from the students table by writing 
 ```
 select * from dareit.students
```
18. thanks to the commands like *INSERT*, *UPDATE*, *DELETE* and others, it is possible to edit the table
19. one of the tasks was to create few more columns with *age* and few more rows --> [the table](https://github.com/inspiritgoldenx/dareit-tasks/blob/main/task_5/table.md)
20. afterwards I created (searched) for a query which answered the question ***what is average age of the students in the class?***
21. the query: 
```
SELECT AVG(ages) as avg_ages
FROM students;
```
the answer ***26,5***
