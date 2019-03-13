# w18brown 

## Documentation
"Brown - Project Team Tracking.docx" - Tracks scrum meetings for the 3 Sprints.

"Brown Final Document.docx" - Examples of each function we finished and what it looks like.

----------------------------
### Downloading and installing mysql.

##### 1) Go to https://dev.mysql.com/downloads/installer/

##### 2) Click the MySQL Server option.

##### 3) Download the appropriate file for your operating system.

##### 4) Follow the install prompts.

----------------------------

### You may need to install node modules with the following command.
  
  $ npm install

----------------------------

### Vue startup instructions. You will need two shells.  

##### 1) On one shell start the client's server with:

  $ npm run dev

##### 2) From the server folder start the server's server with:
  (Linux/Mac)
  $ npm start
  (Windows)
  $ npm run winstart

  You may need to run npm install -g nodemon (-g stands for global)

----------------------------
### Setting up MySql with a non-root user:

  The following instructions for the unix/mac command line log in as root, create the specific account to be used in the code, confirm visually, and exit.

##### 1 Unix/Mac) Logs in as root to allow for the creation of accounts.
  
  $ mysql --user=root mysql  

##### 1 Windows) Log into mysql shell from start menu.
    
##### 2) Identified by is the password
  
  mysql> create user 'browncar'@'localhost' identified by 'brown'; 
  
##### 3) Give permission to use all databases
  
  mysql> grant all privileges on *.* to 'browncar'@'localhost' with grant option;  
  
  Note: markdown has removed the asterisk above on github.  If viewing from github, please use:
  mysql> grant all privileges on \*.\* to 'browncar'@'localhost' with grant option;

##### 4) Optional. Your new user should be listed.
  
  mysql-> select user from mysql.user;  

##### 5) Exit mysql.

  mysql> \q 

  Note: You will need to have the password and username in your mysql match that in the newStart.js file (possibly insertTable.js as well). 
  
----------------------------
### Setup the caraway database:

##### 1 Unix/Mac) Log in to mysql.
  
  $ mysql -u root -p
  
##### 1 Windows) Log into mysql shell from start menu.
  
##### 2) Create an empty caraway database. 
  
  mysql> create database caraway;
  
##### 3) Log out of mysql.
  
  mysql> \q
  
##### 4) Download the caraway.sql file from shared drive **********************
  
##### 5 Unix/Mac) Import the caraway table into my sql from the command line.
  
  $ mysql -u root -p caraway < caraway.sql
  
##### 5 Windows) Import the caraway table into my sql from the command line. Note: your mysql path in quotes may be different.
  
  $ "C:\Program Files\MySQL\MySQL Server 5.7\bin\mysql.exe" -u root -p caraway < caraway.sql
