# Cafe-Dynamic-Web-Application
In this challenge, I undertook 7 tasks to help a café implement online ordering for customers and enable café staff to view submitted orders. The existing website architecture hosted on Amazon S3 was insufficient to meet the new business requirements, necessitating the creation of a dynamic web application hosted on an Amazon EC2

Table of Contents
Task 1: Setting Up the Hosting Environment
Task 2: IDE and Web Server Configuration
Task 3: Making the Website Accessible
Task 4: Installing the Café Web Application
Task 5: Updating PHP Timezone Configuration
Task 6: Duplicating the Café Web Application
Task 7: Verifying the New Café Web Application
Task 1: Setting Up the Hosting Environment

Configured an Amazon EC2 instance to host the café's dynamic web application.
Utilized AWS Cloud9 as my integrated development environment (IDE) for development tasks.
Checked the status of essential components, including the web server, database, and PHP.
Started and set up the web server and database to ensure they run automatically.

Task 2: IDE and Web Server Configuration
Set up AWS Cloud9 to facilitate web development.
Created a symlink to link the AWS Cloud9 editor workspace to the web server's directory.
Adjusted ownership permissions to enable editing of web server files.
Created a basic test webpage and saved it as index.html within the html directory.

Task 3: Making the Website Accessible
Configured the inbound rules in the instance Security Group to allow HTTP traffic on TCP port 80 from anywhere.

Task 4: Installing the Café Web Application
Downloaded and extracted necessary web application files.
Moved the café application files to the web server's document root.
Configured application parameters using AWS Systems Manager Parameter Store.
Configured the MySQL database to support the café application.

Task 5: Updating PHP Timezone Configuration
Adjusted the PHP configuration to set the timezone to "America/New_York."
Restarted the webserver to apply the timezone configuration.

Task 6: Duplicating the Café Web Application
Created an Amazon Machine Image (AMI) from the existing EC2 instance to duplicate the web application.
Established a static internal hostname and generated a new key pair for the EC2 instance.
Created a new AMI named "CafeServer."
Copied the AMI to another AWS Region (Oregon).
Launched a new EC2 instance from the copied AMI with specific criteria to match production requirements.
Established the necessary AWS Systems Manager parameters in the new AWS Region.

Task 7: Verifying the New Café Web Application
Confirmed the successful launch of the new ProdCafeServer instance in the Oregon Region.
Tested the café web application's functionality by accessing it and placing orders.
By completing these tasks, the café now has a dynamic web application that can serve customers, support development, and host the production environment in accordance with the new business requirements.
