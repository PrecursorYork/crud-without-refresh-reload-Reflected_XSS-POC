# crud-without-refresh-reload-Reflected_XSS-POC

+ Exploit Author: PrecursorYork
  
  # Vendor Homepage

+ https://www.sourcecodester.com/php/17146/crud-create-read-update-delete-without-page-reloadrefresh-using-php-and-mysql-source-code
  
  # Overview

+ CRUD-without-refresh-reload Reflected XSS POC is susceptible to a significant security vulnerability that arises from insufficient protection on the 'username' & 'city' parameters in the fetch_data.php & add_user.php file. Attackers can inject malicious JavaScript code into website databases, and when victim users extract and load this JavaScript code, they will be attacked.
  
  # Vulnerability Details

+ Affected Version: CRUD (Create, Read, Update, Delete) Without Page Reload/Refresh Using PHP and MySQL with Source Code V1.0

+ Vulnerable File: /fetch_data.php

+ Parameter Names: username & city

+ # Description

+ Due to the lack of proper input validation and purification for the 'username' & 'city' parameter, attackers can save malicious JavaScript code in the database by inputting it. When the victim accesses the database, malicious code will be loaded, causing the visitor to be attacked.

# Proof of Concept (PoC) :

+ Simulate inputting certain malicious JavaScript code and submit the results to save in the database:

![image](https://github.com/PrecursorYork/crud-without-refresh-reload-Reflected_XSS-POC/raw/main/1.png)

+ When refreshing the page again, the JavaScript code will be triggered because the malicious code in the database is extracted, displayed, and loaded by the browser:
  ![image](https://github.com/PrecursorYork/crud-without-refresh-reload-Reflected_XSS-POC/raw/main/2.png)
  ![image](https://github.com/PrecursorYork/crud-without-refresh-reload-Reflected_XSS-POC/raw/main/3.png)
  ![image](https://github.com/PrecursorYork/crud-without-refresh-reload-Reflected_XSS-POC/raw/main/4.png)
