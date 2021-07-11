BTC price volatility
====================
Agenda:
-------
The Bitcoin price keep changing due to multiple factors that affects the market. 
To have a better picture, our goal is to understand its daily volatility for year 2020.

Pre-requisites:
--------------
In order to run this spark job on your local machine, following setup are needed:
1. IntelliJ Editor (to read run the code, and change some hardcoded values when needed)
2. Git bash (to clone the project)
3. postgreSQL-42.2.4 (with user: "postgres" and password: "Carrom@123"). 
     Rest all the settings for database selection, connection URL etc are default
4. winutils.exe and set the environment variable named HADOOP_HOME to this file location
  
Steps to clone and run the project:
-----------------------------------
1. Nevigate to repository https://github.com/shreyamoghe/Project_BTCDailyPriceVolatility
  
  ![image](https://user-images.githubusercontent.com/13486101/125192917-a86a9c00-e267-11eb-9f85-6e2fc62e5ce1.png)

2. Open Git Bash where you would like to clone this project.

    ![image](https://user-images.githubusercontent.com/13486101/125193077-4eb6a180-e268-11eb-9d4c-746b8202ff57.png)

3. After successful project cloning you will have the project structure as below:
     ![image](https://user-images.githubusercontent.com/13486101/125193351-97bb2580-e269-11eb-89d9-4e60e2c9684d.png)

4. Open the project on your IntelliJ by nevigating to the location same as Step 2
5. 
  ![image](https://user-images.githubusercontent.com/13486101/125193216-ef0cc600-e268-11eb-8883-4ba3fb698e82.png)

5. In postgres create a table "input_btc" in default "postgres" database:

    ![image](https://user-images.githubusercontent.com/13486101/125193626-0351c280-e26b-11eb-9a65-44f3b34f8d7c.png)
    

6. Run the 2 jobs:
       - InputDataMain - right click and select run InputDataMain - to get the json data from URL to postgres table
       - Main  - right click and select run Main - to get the standard deviation resuls
