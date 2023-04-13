# task 5
## the main goal of the task was to learn how to create Cloud SQL instance
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
10. 
11. 
12. 
13. 








what is average age of the students in the class?

SELECT AVG(ages) as avg_ages
FROM students;

26,5
