This is a brief summary of what skills this lab project taught me and my understanding of SQL itself as well as some of it's operators.

#The goal of this query is to Retrieve after hours failed login attempts
![image alt](https://github.com/KoMcGill62/GoogleCybersecuritySpecialization/blob/ee06ea220685e3c8681cd2c69fee857ed5de9c17/Apply%20filters%20to%20SQL%20queries.jpg)

SELECT *
FROM log_in_attempts
WHERE login _ time > '18:00' AND success = 0;

I start by using the SELECT operator to select all failed login attempts. I further specify my query using FROM to indicate where I want the data points to come from. I then use the WHERE operator to show what specific filter I want to use. I then use > command to indicate I only want failed attempts after 6pm. The AND command ensures it is not only a login attempt after 6pm but also a 0 which is the login failure value.
