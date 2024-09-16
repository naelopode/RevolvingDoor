# ![image](static/favicon.svg) Revolving Door Watch
Application tracking MEPs that left the European parliament after the 9th term.

Features :
1. Detecting changes in Twitter bios
2. Detecting news from Google alerts

## Login page
Protected login to prevent. Login is shared between users for now.
![image](img/RDW_login.png)

## Main page
Allows the user to read the twitter bio of all non-reelected MEPs.
![image](img/RDW_main.png)

## Difference in bio
Highlight difference in bios that could reflect a change of job title.
![image](img/RDW_difference.png)

## News aggregation
Shows all recent news from each MEPs. Allows user to filer by date.
![image](img/RDW_News.png)

## Installation
One docker handles the database (running MongoDB), the other docker runs the code of:
1. The webserver running Flask
2. A Twitter script using [TweeterPy](https://github.com/iSarabjitDhiman/TweeterPy). Checking for changes in twitter bios.
3. A script checking for changes in the RSS feeds of the google alerts linked with MEP's.
![image](img/schematic.png)

All parameters, twitter logins, web UI logins, API keys are stored in a config file. 

## TODO
1. Dockerize the custom codes.
2. Add the ability to manually add people to stalk ?
3. Add alerts when name are detected in other datasets ?
