# Cover letter

Vlad's main speciality is data integration and data processing. He has 10+ years (15+ years in Software Engineering) hands on experience in various data integration platforms/products and some recent exposure to AWS technology stack.


## AWS
(buzz words: Fargate, ECS, EC2, RDS, S3, Cognito, Athena, Lambda, Docker, Terraform)

#### PoC for Fonterra.
The main goal of this exercise is to try to migrate an on-prem system to the AWS cloud. The system is a complex/mature application (5 years old) that consists of multiple main modules: CMS (Silverstripe), API (Java, Tomcat), Mobile Apps (4 hybrid apps), ETL (Pentaho), DB (Postgres). The exercise can be described as the following:
* Converting the existing modules to be able to run in docker
* Design/implement docker infrastructure (dockerfiles, networking, volumes etc)
* Design/configure AWS Fargate, AWS ECS, AWS EC2, AWS RDS (postgres), AWS S3 to be able to accomodate and run the system entirely in cloud
* Automate build/deployment to AWS using Terraform scripts

#### PoC for Scion
Design a new system based on AWS technology stack that consists of API, mobile app and file system storage. The main purpose of the system is to provide a platform for public users that can be used to report observations about pests in NZ.
* Design and implement API using AWS Lambda. Two programming languages have been trialed: Golang and Java
* Implement OAuth2 authentication with 3rd party API using AWS Cognito
* Develop file system storage to store/retrieve/search users media files using AWS S3 and AWS Athena

##

#### Salesforce
* Current Salesforce certificates (App builder, Platform Developer, Development Lifecycle & Deployment)
* Broad experience with REST and SOAP Salesforce API
* Identity provider & SSO authentication

#### Integration
* Pentaho ETL. Designed and implemented a large number of ETL integration processes for a Fonterra project (5+ years).
* Apache camel. Developed multiple application integration background processes massaging/exposing data.
* Informatica cloud services and cloud data integration. Attended a multiday course/workshop to get familiarized with Informatica offerings in data integration/processing field. Certificate pending.
* Mule. Supported some existing mule processes for NZ Lotteries project. Recently attended an extensive multiday Mule4 training/workshop to get familiarized with new features of Mule 4. Certificate pending.

#### Authentication
* OAuth2 various authentication flows: JWT, Resource owner (username/password), SAML
* SSO
* Active directory

#### Design / Implement API
* Strong experience in designing/implementing/consuming restful APIs
* Performance optimization
* Designing APIs for occasionally connected mobile apps (data footprint optimization; incremental interaction; combined/composite APIs)

#### Databases
* Deep knowledge of Postgres DB. Designing data structures. Developing stored procedures/functions. Implementing hybrid store in Postgres (RDBMS + JSON storage)
* Some exposure to RDBMS DBs (MySQL, MS SQL and Oracle) and Key-value stores (Mongo, Riack)

#### Search
* Good experience in Elastic Search engine. Designing data structure and search queries. Consuming REST APIs.
* Good but rusty experience in Apache Lucene/Solr search engine.

## Opensource
A good example of the way how I code and document, check the source code in github.
### Bluetooth projects
Very unique and large (25k+ lines of code) opensource projects (multiple modules) that have been designed and implemented from scratch to provide Java API to work with Bluetooth stack (Bluetooth Smart). Publicly available from the Central Maven repository. Fully automated build system / release process / code analysis in travis / maven repository / codacy. Large number of unittest (some modules have 95% of unittest code coverage, some 50%). Design overview and code: https://github.com/sputnikdev/bluetooth-manager
#### Java Bluetooth Manager
An API that hides all complex logic of dealing with the unstable by its nature Bluetooth technology. Automatic disaster recovery, "configure and forget" design principles employed to provide robust and extensive API.

source: https://github.com/sputnikdev/bluetooth-manager

#### Bluetooth GATT parser
A unique project that provides Java API for automatic serialization/deserialization of Bluetooth GATT messages/structures by using XML definitions.

source: https://github.com/sputnikdev/bluetooth-gatt-parser

#### OpenHab Bluetooth Binding (plugin)
A very popular (200-400 downloads per month) 3rd party binding that provides extensive support for Bluetooth Smart devices in OpenHab (Eclipse Smart Home) home automation system (uses the Java Bluetooth Manager and the GATT parser projects under its bonnet):

* source: https://github.com/sputnikdev/eclipse-smarthome-bluetooth-binding
* official forum thread: https://community.openhab.org/t/3rd-party-bluetooth-binding-beta-testers-needed
* download stats: https://bintray.com/sputnikdev/org.eclipse.smarthome.binding.bluetooth/eclipse-smarthome-bluetooth-binding#statistics

---
#### Electronic Suspension System
A DIY project for full-suspension bikes to automatically operate settings of shock absorbers in real time in accordance with different terrain types and riding styles). An article about this system has become the most popular article of the month with:
* 11500+ reads bikerumor.com (in English, NOTE some videos are broken, see links below): https://bikerumor.com/2012/11/26/hacktastic-diy-automatic-electronic-suspension-lockout-w-stealth-remote-buttons/
* 80000+ reads habrahabr.ru (in Russian): https://habr.com/post/158449/
* videos:
    * overview:
        * https://www.youtube.com/watch?v=vhOzcJZVryw
		* https://www.youtube.com/watch?time_continue=8&v=FK0hFBXIHro
	* mobile app:
	    * https://www.youtube.com/watch?v=Vsa-XM66wis
		* https://www.youtube.com/watch?v=tHbQ-7qTYyg
		* https://www.youtube.com/watch?v=n8UkAGkWqZ8

* Caused some patent infringements and complaints from a largest bike manufacturer in Europe and USA as the system has been implemented before some patents had been registered describing the some parts of the system
* Developed an electronic circuit board based on AVR microcontroller with various sensors: accelerometers, gyroscope, magnetometer, speed, cadence. The board was specially designed to be accommodated in a very limited space (inside of the bike frame) so it is very compact and lightweight
* Created an efficient communication protocol (in C++ and Java) between AVR microcontrollers and Android devices via bluetooth, which allowed dramatically minimize the amount of traffic between devices and led to sufficient increase of the device run time
* Implemented an android application to monitor system activity, calibrate servos and control some settings, which communicates with bike microcontroller via bluetooth
* Developed embedded application in C++ for AVR microcontroller based on finite-state machine to automatically control bike suspensions in real time accordingly to various onboard sensors
* Source code: https://github.com/vkolotov/suspension-system

#### Valve / digital headphones amplifier
A DYI project to create a piece of Hi-FI equipment based on Raspberry Pi, high definition audio DAC, very low noise power supplies (separate supplies for RPI and DAC to reduce power line noise), a true HI-FI valve amplifier and python as a programming language to control the amp. This project deserves to be mentioned as it is a finished "product" that I use every day. The amp runs Logitech Media Server that allows to play any format of music (Spotify, streaming, mp3 etc). The amp can be controlled via web browser or by using several hardware buttons (play/pause/select playlist etc). Apart from playing musing, the amp implement several safety features as it gets hot while playing, such as:
* Emergency shutdown if temperature threshold is exceeded
* Monitoring presence of listener via bluetooth (turns off if BT his/her device is out of range)
* Playback timeout via linux cron

Source code: https://github.com/vkolotov/tube-amp

