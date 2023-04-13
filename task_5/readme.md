# task 5
## the main goal of the task was to learn how to create Cloud SQL instance
1. first of all I opened **Cloud SQL** from the *Navigation Menu* in Google Cloud and clicked ***CREATE INSTANCE***
2. after that, I chose the **PostgreSQL** (second option) and filled the information there
3. I have added: Instance ID = *dareit-pg* (because the instance-id needs to be unique within the GCP project), Password = *whatever* (I made some up), Database version = here I chose *PostgreSQL 14* because that is the version of the engine, configuration to start = I chose *Sandbox* (because it's for me to train)
4. next step was to customize the instance, so I went to *Connections* where I chose **Public IP** , then I chose **ADD NETWORK** (under the Authorised Networks section) - thanks to that, we will be able to add an IP from which packets will be allowed to the Database Instance
5. so after that, I have googled my IP number and pasted it into *Newtork* field








what is average age of the students in the class?

SELECT AVG(ages) as avg_ages
FROM students;

26,5
