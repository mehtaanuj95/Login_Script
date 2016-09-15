# Login_Script
A very basic login script. Adapted from cs50.
This script follows mvc - model view controller pattern. Feel free to edit or modify it.

For setting this up, you would need to perform following steps.
 Download and install xampp for windows.
 Fork this repository and then Clone it inside the htdocs folder.
 Now, go to C:\xampp\apache\conf\extra  and then open up httpd-vhosts.conf
 Append this code at the end of this file


        <VirtualHost *:80>
            DocumentRoot "C:/xampp/htdocs"
            ServerName localhost
        </VirtualHost>
        
        <VirtualHost *:80>
            DocumentRoot "C:/xampp/htdocs/Login_Script/public/"
            ServerName mywebsite.com
        </VirtualHost>


 The previous step configured our virtual hosts directory. By appending this content into it, we are insuring that the server takes the public folder insode Login_Script as its root. If this step is not carrierd out, then an error will be displayed indicating too many redirects. Also we name it by mywebsite.com. You are free to choose any name here of your choise. But be cautious not to change the servername from localhost to anything else in 1st virtual host tag.
 
 Now that you have configured your virtual host, now you need to edit the windows host file. Go to   C:\Windows\System32\drivers\etc  and open up  'hosts' file. At the end of it, append the following data- 


        127.0.0.1 		mywebsite.com


 Make sure that the servername mentioned in second virtual host tag in httpd-vhosts.conf is exactly tha same as mentioned here. By doing this we are telling the computer to go to mywebsite.com when localhost in opened. By default, ip address of localhost is 127.0.0.1. This is called the loopback ip address.
 
 Now that we have configured these files, we must start our server and mysql from xampp.
 Open up phpmyadmin and import the file db.sql.
 All right ... You are done with configuration part. Open 'http://mywebsite.com' in your favourite web browser.

You can login with following credentials.
username : skroob
password : 12345
or you can register as a new user.

** Note : This script was given as an distribution code in the problem set 7 of Harvard's CS50 course.

** This tutorial is written by Anuj Bhai Mehta. If it proves useful, give a mention.
