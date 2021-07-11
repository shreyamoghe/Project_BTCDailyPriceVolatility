BTC price volatility
====================
Agenda:
-------
The Bitcoin price keep changing due to multiple factors that affects the market. 
To have a better picture, our goal is to understand its daily volatility for year 2020.

Pre-requisites:
--------------
In order to run this spark job on your local machine, following setup are needed:
1. IntelliJ IDEA Editor (to read run the code, and change some hardcoded values if needed)
2. Git bash (to clone the project)
3. postgreSQL-42.2.4 (with user: "postgres" and password: "Carrom@123"). 
     Rest all the settings for database selection, connection URL etc are default
4. winutils.exe and set the environment variable named HADOOP_HOME to this file location
  

Steps to setup HADOOP_HOME:
---------------------------
1. Download winutils from https://github.com/steveloughran/winutils/blob/master/hadoop-2.7.1/bin/winutils.exe
   
   ![image](https://user-images.githubusercontent.com/13486101/125194098-68a6b300-e26d-11eb-9d88-353c12ef3790.png)
   
2. Create some recursive directories in C directory as  "BigDataLocalSetup" --> "hadoop" --> "bin"
3. Inside "bin" and paste the downloaded winutils.exe file
     
     ![image](https://user-images.githubusercontent.com/13486101/125194290-38134900-e26e-11eb-9899-34771695fcb1.png)
     
4. Go to environment variables and setup your HADOOP_HOME and also it to "path" variable as follows:
     
      ![image](https://user-images.githubusercontent.com/13486101/125194476-19618200-e26f-11eb-9ee6-5a6353668f01.png)
      
      ![image](https://user-images.githubusercontent.com/13486101/125194612-af95a800-e26f-11eb-8fc2-cd251aaeacdb.png)
      


Steps to clone and run the project:
-----------------------------------
1. Clone the project in your machine and open it in IntelliJ IDEA

2. Open the project on your IntelliJ by nevigating to the location same as Step 2

  ![image](https://user-images.githubusercontent.com/13486101/125193216-ef0cc600-e268-11eb-8883-4ba3fb698e82.png) 

3. After successful project cloning you will have the project structure as below:

     ![image](https://user-images.githubusercontent.com/13486101/125193351-97bb2580-e269-11eb-89d9-4e60e2c9684d.png)

4. In postgres create a table "input_btc" in default "postgres" database:

    ![image](https://user-images.githubusercontent.com/13486101/125193626-0351c280-e26b-11eb-9a65-44f3b34f8d7c.png)
    
5. Run the 2 jobs:
       - InputDataMain - right click and select run InputDataMain - to get the json data from URL to postgres table
       - Main  - right click and select run Main - to get the standard deviation resuls
