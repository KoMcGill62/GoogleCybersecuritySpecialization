# This is a brief summary of what skills this lab project taught me and my understanding of SQL itself as well as some of it's operators.

## The goal of this lab query is to retrieve after hours failed login attempts


![image alt](https://github.com/KoMcGill62/GoogleCybersecuritySpecialization/blob/ee06ea220685e3c8681cd2c69fee857ed5de9c17/Apply%20filters%20to%20SQL%20queries.jpg)

SELECT *

FROM log_in_attempts

WHERE login _ time > '18:00' AND success = 0;

I start by using the SELECT operator to select all failed login attempts. I further specify my query using FROM to indicate where I want the data points to come from. I then use the WHERE operator to show what specific filter I want to use. I then use > command to indicate I only want failed attempts after 6pm. The AND command ensures it is not only a login attempt after 6pm but also a 0 which is the login failure value.

## The goal of this lab query is to retrieve login attempts on specific dates

![image alt](https://github.com/KoMcGill62/GoogleCybersecuritySpecialization/blob/69fd1a64b81d956e51b4291821aa7060c00d69d6/folder/SQL2.png)

SELECT *

FROM log_in_attempts

WHERE login_date = '2022-05-05' OR login_date = '2022-05-08';

Again beginning with SELECT operator to select all data entries that apply I use FROM operator to choose which table for the system to use. I then use WHERE to indicate the conditions for the filter. Those conditions being the days of 2022-05-09 or 2022-05-08. I used the = operator to apply the filters of only entries on that day. I used the OR operator to make sure both days are added to the results.

## The goal of this lab query is to retrieve login attempts outside of Mexico

![image alt](https://github.com/KoMcGill62/GoogleCybersecuritySpecialization/blob/f07ac8b1d425a9d74248534b0f409fb4095c76d3/folder/SQL3.png)

SELECT *

FROM log_in_attempts

WHERE NOT country LIKE 'MEX%';

Once again starting with SELECT I move to FROM to choose which table the system needs to use. Then using WHERE and NOT in conjunction I filter Mexico from the results. I use % as a wildcard because some entries use Mex.

## The goal of this lab query is to retrieve employees in marketing

![image alt](https://github.com/KoMcGill62/GoogleCybersecuritySpecialization/blob/ba457386941c8b3f054d77a8361c035a0e292300/folder/SQL4.png)

SELECT *

FROM employees

WHERE department = 'Marketing' AND office LIKE 'EAST%';

I use SELECT for all data entries that apply. I use FROM to choose which table the system needs to query and WHERE with = to make sure the results were from the marketing department. I used the AND and LIKE operators in conjunction to ensure the data points were from the multiple different east building offices. I again used % as a wildcard to get any of the east buildings.

## The goal of this lab query is to retrieve employees in finance or sales

![image alt](https://github.com/KoMcGill62/GoogleCybersecuritySpecialization/blob/f041a2ae21642bf379eb39259ae284a439222663/folder/SQL5.png)

SELECT *

FROM employees

WHERE department = 'Finance' OR department = 'Sales';

SELECT operator to select all data entries that apply. I then use the FROM operator to choose which table for the system to use. I then use the WHERE operator with the = operator to make sure the results were from the finance department. I then use the OR operator to include the sales department in my filter

## The goal of this lab query is to retrieve employees not in IT

![image alt](https://github.com/KoMcGill62/GoogleCybersecuritySpecialization/blob/f041a2ae21642bf379eb39259ae284a439222663/folder/SQL6.png)

SELECT *

FROM employees

WHERE NOT department = 'Information Technology';

SELECT operator to select all data entries that apply. I then use FROM operator to choose which table to use. I use the WHERE and NOT operators in conjunction to make sure the Information Technology department was excluded from the filter results.
