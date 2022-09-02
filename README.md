# JavaProject
*This is a Java Project for (GROUP 23)
This is a project named "Hostel Allocation System" it gives users opportunity to apply for hostels at home even before they come to campus.
This project is incomplete at moment.
The StartApp file is main file that starts the project 

*This project is linked to a database.
You can create a database with you own database name or using the Default project databse name "pocbase" using mysql or xampp
the database should contain this tables.
"user_register", "user_login", "admin_login", "forgot_pass", "user_apply".

You can also use the queries below 
Note: If you create your own database Name make changes in the code where ever the database name was used.

CREATE TABLE `user_login` (
   `idUserAccount` int unsigned NOT NULL AUTO_INCREMENT,
   `FirstName` varchar(45) NOT NULL,
   `LastName` varchar(45) NOT NULL,
   `UserName` varchar(45) NOT NULL,
   `Password` varchar(45) NOT NULL,
   PRIMARY KEY (`idUserAccount`),
   UNIQUE KEY `idUserAccount_UNIQUE` (`idUserAccount`),
   UNIQUE KEY `UserName_UNIQUE` (`UserName`)
 ) ENGINE=InnoDB AUTO_INCREMENT=9 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci

CREATE TABLE `user_register` (
   `iduser_register` int unsigned NOT NULL AUTO_INCREMENT,
   `firstname` varchar(45) NOT NULL,
   `lastname` varchar(45) NOT NULL,
   `username` varchar(45) NOT NULL,
   `address` varchar(45) NOT NULL,
   `dateOfBirth` date NOT NULL,
   `email` varchar(45) NOT NULL,
   `country` varchar(45) NOT NULL,
   `contact` int NOT NULL,
   `stat` varchar(45) NOT NULL,
   `sex` varchar(45) NOT NULL,
   `password` varchar(45) NOT NULL,
   PRIMARY KEY (`iduser_register`),
   UNIQUE KEY `iduser_register_UNIQUE` (`iduser_register`),
   UNIQUE KEY `username_UNIQUE` (`username`)
 ) ENGINE=InnoDB AUTO_INCREMENT=52 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci
 
 
 CREATE TABLE `admin_account` (
   `idadmin_account` int NOT NULL AUTO_INCREMENT,
   `Firstname` varchar(45) NOT NULL,
   `Lastname` varchar(45) NOT NULL,
   `Hostelname` varchar(45) NOT NULL,
   `Username` varchar(45) NOT NULL,
   `Password` varchar(45) NOT NULL,
   PRIMARY KEY (`idadmin_account`),
   UNIQUE KEY `idadmin_account_UNIQUE` (`idadmin_account`),
   UNIQUE KEY `Username_UNIQUE` (`Username`)
 ) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci
 
 
 
 CREATE TABLE `user_apply` (
   `iduser_apply` int NOT NULL AUTO_INCREMENT,
   `hostelname` varchar(45) NOT NULL,
   `gender` varchar(45) NOT NULL,
   `roomtype` varchar(45) NOT NULL,
   `file` varchar(45) NOT NULL,
   `passportpic` varchar(45) NOT NULL,
   PRIMARY KEY (`iduser_apply`),
   UNIQUE KEY `iduser_apply_UNIQUE` (`iduser_apply`)
 ) ENGINE=InnoDB AUTO_INCREMENT=8 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci
 
 CREATE TABLE `forgot_pass` (
   `idforgot_password` int NOT NULL AUTO_INCREMENT,
   `username` varchar(50) NOT NULL,
   `password` varchar(50) NOT NULL,
   PRIMARY KEY (`idforgot_password`),
   UNIQUE KEY `idforgot_password_UNIQUE` (`idforgot_password`)
 ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci
