![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/poster.PNG)
# SQL-Murder_Mystery_Investigation
This is an SQL project showing how simple SQL functions are used to investigate a murder case using all the required information in a database. This project shows how powerful SQL can be in investigating issues such as crime and so on. 

In this project, there will be a full detailed explanation on how SQL was used for all the investigative process and clues gotten to solve the murder mystery and discover the murderer.

There's been a Murder in SQL City! The SQL Murder Mystery is designed to be both a self-directed lesson to learn SQL concepts and commands and a fun game for experienced SQL users to solve an intriguing crime.

## Problem Statement

A crime has taken place in a **gym** at **SQL City**  and the detective needs your help. The detective gave you the **crime scene report**, but you somehow lost it. You vaguely remember that the crime was a **murder** that occurred sometime on **Jan.15, 2018** and that it took place in **SQL City**.

## SQL Investigation Process

Start by retrieving the corresponding crime scene report from the police department’s database.

Firstly, we need to know the names of all the tables in the database and also get the **Entity Relation Diagram (ERD)** of the database to understand how the tables are being related. *Image below....*

### Table names
![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/murder%20table.PNG)   


### ERD
![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/murder%20ERD.PNG)


Then next we query the **crime_scene_report** table to get the info about the murder that happened on **Jan.15 2018** and it took place in **SQL City**. *Using the below SQL code….*

![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/1.PNG)

The description gotten say that the security footage says that there were two witnesses which are: 

* **Witness 1:** lives at the last house on **Northwesthern Dr.**
* **Witness 2:** named **Annabel** and lives somewhere on **Franklin Ave.**

Using the above info, we will need to get the identity of the witnesses in order to know what info they gave in their interview sessions. We will get better clue there. *Using the SQL code below...*

![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/2.PNG)

The above info shows that the name of **Witness 1** is **Morty Schapiro** with **ID 14887**, **License_id 118009**.

To also get the info of **Witness 2**. *Using the SQL code below….*

![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/annabel.PNG)

The above info shows the name of  **Witness 2** is **Annabel Miller** with **ID 16371** and **License_ Id 490173**.

Since we have gotten the names and IDs of the two witnesses, we now need to check the **Interview** table to know what info the 2 witnesses gave when interviewed to further the investigation. *Using the SQL code below…*

![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/3.PNG)

From the info in the two witnesses interview, it says:
* **Witness 1** heard the gunshot and saw a man ran out with a membership bag that start with **‘48Z’** which is only used by **gold** members and also got a car of plate number **“H42W”**.
* **Witness 2** saw the murder happened and recognize the killer from the gym last week on **Jan 9th**

With info above we now try to write a query that bring out the info on members that has ID that starts with **‘48Z’** and are **gold** members. *Using the code below…*

![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/4.PNG)

It shows **Joe Germuska (ID 48Z7A)** and **Jeremy Bowers (ID 48Z55)** as the two suspects that has ID that start as **‘48Z’** and are also **gold** members.

Since we have gotten our two suspects using the membership_id clue and their membership_status as **gold** members. Now we need to know the real murderer through the plate number **“H42W”**. But we need to get the **License_id** of the two Suspects first before we can get their car plate number to check if any match with what **Witness 1** said. *Using the SQL code below..*

![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/5.PNG)

After getting license Id of the two suspects, we can now check the plate number of the suspect’s cars to know which is correlated with the info given by **Witness 1**. *Using the SQL code below..*

![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/6%20(2).PNG)

Wow!!! Finally we have gotten the MURDERER which is **Jeremy Bowers** one of the suspects and he also has the plate number **"0H42W2"** as witnessed by **Witness 1** who said the saw murderers car plate number **“H42W”.**

![](https://github.com/FreshDAnalyst/SQL-Murder_Mystery_Investigation/blob/main/final.PNG)

Though the murderer has been discovered but there is still more to investigate in the database using **SQL queries**. This is just the beginning
