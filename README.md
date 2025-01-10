# **Integrated Justic Records Platform**

A INTRODUCTION TO DATABASES (CS-UY-3083) Course Project Taught By Prof. Arfaoui 
---

## **Table of Contents**

1. [Overview](#overview)  
2. [Design](#Design)  
3. [Usage](#usage)  

---

## **Overview**
**NOTES:**
- All data displayed on this project is psuedo data created for this project no data is supposed to reflect any individuals
- This repo is purely used for hosting to view full version history visit: https://github.com/jw7914/Jail_Database


**Integrated Justic Records Platform** is a Flask-based web application that interacts with a MySQL relational database tgat allows users to view records of inmates, officers, crimes, fines, and other related data which should reflect an justice system. 

---

## **Design**
- Security Features
  - Route protection through use of Flask sessions that are only created during sucessful login  (through lookup of backend table)
  - Privileges and roles established on the database in order to approiately assign views and roles of different users (public users, admin, officers)
  - Password hashing ulitized to protect user credentials on potential leaks (and passwords are not visible to admins)
- General Choices
  - In order to sucessfully register for an account, an user needs to be an officer (enforced through requiring badge number to register)
  - Only officers can search up other officers (search for officers only avaible on officer login page)
  - Admin login is created with raw SQL (no registration from front-end needs to be configured) but allows for creating, reading, updating, and deleting (CRUD) infromation related to users(people who have registered), officers, and criminals.
  - 
---

## **Overview**
Please feel free to interact with this project at: https://jaildb.vercel.app/
If you want to test the officer view please use the follow credientials:
username: githubuser
password: test

Admin login is not acessible to the public however here are some screenshots that show the admin view:

**Users**
![Users Dashboard](/users.png)
**Criminals**
![Criminals Dashboard](/criminals.png)
**Officers**
![Officers Dashboard](/officers.png)


