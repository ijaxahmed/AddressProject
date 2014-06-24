AddressProject
==============

A sample project crawl a website(e.g www.abc.com/address.php, http://www.abc.de/impressum.php) to monitor address. When address has changed will be save in database. Following technologies used in this project, JTA/Hibernate, Ejbeans (Session, Entity),Junit, jsoup library, Moduler development, Maven, Design Patterens(Facad). for More details please look at ReadMe

URL Monitor Task
=============================
-consists of two projects
	-AddressProject: A project consists of different modules
	- ClientWeb: A web client to interact with AddressProject Modules


AddressProject
============================

Implementation:
----------------------------
-Project implemented in modules, consists of two modules
	- AddressBusinessModule : Contains business logic
	- Persistance module : performs database operations
	- Project can be extended with other module easily

-Oracle data base
	- jboss datasource file provided in resource folder

-pom.xml

AddressBuinessModule
---------------------------
- AddressBusinessModule implemented core business logic fo URL monitoring
- Design Patteren - Facad
- consists of following
	- Ejbean to monitor URLs
	- unit tests
	- doc
	- pom.xml
	-dependencies
		- Jsoup : for URL Crawling
		- javax.mail : to send email
		- Junit : for unit testing
		- Persistence Module

PersistenceModule
---------------------------
- AddressBusinessModule implemented database interaction
- 
- consists of following
	- Entity beans for code objects
	- session beans for database operation	
	- JPA/Hibernate implementation
	- unit tests
	- doc
	- pom.xml
	-dependencies
		- Hibernate : JPA implementation
		- oracle : oracle driver
		- Junit : for unit testing

Webclient
------------------------
Consists of following
- jsp view
- Controller servlet
- pom.xml

Resource folder AddressProject\resources
------------------------
-ReadMe
-Application Architecture diagram
-A sequence diagram
-Database schema
-jboss db datasource 



Things to be improve/ further implement
----------------------------
- Logging 
- Exception Handling
- Ejbean Timer: to trigger continues action after defined interval
- Dynamic Configuration : to define recipient email etc
- 



