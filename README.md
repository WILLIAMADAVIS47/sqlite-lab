# SQLite Lab

## Overview
This lab demonstrates setting up SQLite and sqlite-web in a GitHub Codespace, importing a dataset, and running SQL queries.

## Tools Used
- SQLite3 3.45.3
- sqlite-web
- GitHub Codespaces

## Steps Completed
1. Created GitHub repository and opened Codespace
2. Installed sqlite3 and sqlite-web
3. Created testsqlite.db using sqlite3 command prompt
4. Launched sqlite-web and accessed portal from mobile browser
5. Imported flights-export.csv into flights table
6. Ran SQL queries using sqlite-web
7. Redid query in sqlite3 command prompt

## SQL Queries

### a) Net Income > 0
SELECT Year, SUM(Num_of_Passengers) AS total_passengers, ROUND(AVG(Num_of_Passengers), 2) AS avg_passengers FROM flights WHERE Net_Income_Fin_Position_ > 0 GROUP BY Year ORDER BY Year;

### b) Net Income < 0
SELECT Year, SUM(Num_of_Passengers) AS total_passengers, ROUND(AVG(Num_of_Passengers), 2) AS avg_passengers FROM flights WHERE Net_Income_Fin_Position_ < 0 GROUP BY Year ORDER BY Year;

### c) All Records
SELECT Year, SUM(Num_of_Passengers) AS total_passengers, ROUND(AVG(Num_of_Passengers), 2) AS avg_passengers FROM flights GROUP BY Year ORDER BY Year;
