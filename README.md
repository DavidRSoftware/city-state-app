To run this program on your local computer you will need to set up your MySQL database as well as substitute the username and password to the username and password of your the database on your local computer in the appropriate locations in the index.js file.
1) Create a database named "citystate".
2) Create a table in that database using the following SQL:
"CREATE TABLE citystatedata (City VARCHAR(50), StateShort
VARCHAR(50), StateFull VARCHAR(50), County VARCHAR(50),
CityAlias VARCHAR(50));"
3) Use the us_cities_states_counties.csv file that is included with this repository
(credits: https://github.com/grammakov/USA-cities-and-states) to load the data to the database.
You might need to modify the path to the csv file to get this SQL to work.
"LOAD DATA INFILE '/us_cities_states_counties.csv' INTO TABLE
citystatedata COLUMNS TERMINATED BY '|' LINES TERMINATED BY
'\n' IGNORE 1 LINES;"
4) Modify user and password names on line 29 and on line 54 and 55 of index.js to fit the username and password of the database on your local computer.