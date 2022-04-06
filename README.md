		
Add PGP Key	
 wget -qO- https://dl.packager.io/srv/opf/openproject/key | sudo apt-key add -	
		
Integrate OpenProject repository in Ubuntu 20.04	
 sudo wget -O /etc/apt/sources.list.d/openproject.list https://dl.packager.io/srv/opf/openproject/stable/12/installer/ubuntu/20.04.repo	
		
Update package	"
 sudo apt update
"	
		
Now install openproject	
 sudo apt install openproject	
"Start configuring OpenProject
 sudo openproject configure	
 domain name use the ip address of the os static ip if available or localhost address
		
Select Default OpenProject 		
		
Configure PostgreSQL		
"To store its data we need a database server, here the OpenProject offers you an option to automatically install “Postgres“, however, if you already have an installed Postgres somewhere or on the same server then you can go for “Use an existing PostgreSQL database” option.

However, here we are going for “Install a new PostgreSQL server and database locally“. Select it, Okay, and then hit the Enter key."	if install first time use install /use install postgres database locally         if you have pre-install postgresssql then use refuse >>that means use existing database	
		
Install Apache Webserver		
		
Set Fully Qualified domain
		
"To access the OpenProject using FQDN, mention the same here. For example, here we are using demo.how2shout.com. You can use whatever you have.

Alternatively, if you want to access it using a server IP address then mention that instead of a domain name."	we can use localhost ip/ static ip / domain	
		
Server Path (optional)		
This is optional. If you want to access your OpenProject web interface under some folder then you can mention it here. For example, let say you already have some website running on your server and to access it you are using your root domain then we cannot use the same domain to access another web platform. Therefore, to solve we can install another website under a subfolder. And the name of that subfolder you can mention here.	/openproject	
		
skip ssl	no	
		
Install Subversion	install	
		
skip smtp	skip	
		
Access OpenProject Web interface	on localhost/ip/domain which is we have mention in qualified domain 	
		
## Default login password is 	admin/admin	After login first time must update default pass
		
##-----------------Backup--------------------------##		
		
		
step 1 - For backup openproject we can use pgadmin	open pgadmin	
		
step 2 - connect / login into sql server	we can see database list and something else	
		
step 3 - we can backup now 	Lets backup	
		
## Others way we can backup openproject from openproject interface	we can backup from open project backup option	
		
###-----------------Restore openproject in new pc------------###
		
		
step 1 -  install sql database and pgadmin 	Follow previous postgres installation and pgadmin installation	
		
step 2 - connect sql database into pgadmin	Lets connect	
		
	127.0.0.1 /loclhost	connection string
		
	5432	default port
		
	postgres	database name
		
	postgres	database user name
		
	pass	database user pass >> if password is not working then alter database usr pass and use new pass
step 3 - After successfully connect database into pgadmin restore existing backup file	Restore openproject backupfile into selected databse	
		
last step copy file system and replace with new file system	/var/de/openproject/files	
		
	## Happy openProject	
