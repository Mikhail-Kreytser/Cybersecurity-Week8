# Cybersecurity-Week8

## Blue
### SQL Injection
#### Use the id parameter in the url to infiltrate the system: /blue/public/staff/salespeople/show.php?id=1 
#### Explore the Database with sqlmap
![alt text](https://github.com/Mikhail-Kreytser/Cybersecurity-Week8/blob/master/Demo/SQLI.gif "SQLI Demo")

### Session Hijacking/Fixation
#### Use the tool to change your PHPSESSID to a logged in user's PHPSESSID: public/hacktools/change_session_id.php
#### Have a user open a malicious website that sets their PHPSESSID to the attacker's PHPSESSID. The user will have to login again. This makes the attacker's PHPSESSID valid.
![alt text](https://github.com/Mikhail-Kreytser/Cybersecurity-Week8/blob/master/Demo/SessionHijacking.gif "Session Demo")

## Red
### Insecure Direct Object Reference
#### Use the public find a Salesperson tool to look for someone. After a Salesperson is found, use the id parameter in the url to look for other people in the system.
![alt text](https://github.com/Mikhail-Kreytser/Cybersecurity-Week8/blob/master/Demo/IDOR.gif "Insecure Direct Object Reference Demo")

### Cross-Site Request Forgery
#### Create a website that has a form that posts to red/public/staff/salespeople/edit.php?id=1. When a logged in user goes the malicious website, the salesperson with id 1 has their information updated.
![alt text](https://github.com/Mikhail-Kreytser/Cybersecurity-Week8/blob/master/Demo/CSRF.gif "Cross-Site Request Forgery Demo")


## Green
### Username Enumeration
#### Go to the main login. If the wrong password is entered and the user exists, the error is bold. If the wrong password is entered and the user does not exist, the error just plain text. 
![alt text](https://github.com/Mikhail-Kreytser/Cybersecurity-Week8/blob/master/Demo/UsernameEnumeration.gif "Username Enumeration Demo")

### Cross-Site Scripting
#### Go leave some feedback and inject code. When a logged in user/admin visits the feedback page. The injected code is ran.
![alt text](https://github.com/Mikhail-Kreytser/Cybersecurity-Week8/blob/master/Demo/XSS.gif "Cross-Site Scripting Demo")

### Cross-Site Scripting + Session Hijacking/Fixation
##### Hypothetically, the malicious code can change the logged in user's PHPSESSID to the attacker's. The code can then refresh the page or redirect to login. The user might think that it was a glitch and login again. By doing that, the attacker's PHPSESSID can now be used to login. The malicious code can also just send the current user's PHPSESSID to the attacker allowing the attacker to use it to login.
