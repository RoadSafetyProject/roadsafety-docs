.. _about:

.. index:: About The Documentation

About The Documentation
=======================
The iROAD documentation is a collective effort and has been developed by the development team and users. While the guide strives to be complete, there may be certain functionalities which have been omitted or which have yet to be documented. This section explains some of the conventions which are used throughout the document.

iROAD is a browser-based application. In many cases, screenshots have been included for enhanced clarity. 
Shortcuts to various functionalities are displayed such as "Maintenance->Data administration". 
The "->" character indicates that you should choose "Maintenance" and then click on "Data administration" in the menu which appears through the browser.


.. index:: What is iROAD 2

What is iROAD 2
===============
Road Safety Management Information System (iROAD) is a software that intends to improve Management of Road Safety in Tanzania.

iROAD enables Car registration and use validity which involves verification of the car registration, 
driver and road license validity by police, customs, or TRA; Capturing, storage and use of traffic 
offence incidents which involves recording of traffic offence incidences when they occur by police or 
reported by the community (witness or victim), notification and-or educating of the offender by police 
about the offence(s) committed and tracking of the payment of fines or court decisions that result from 
the offence(s); Recording and transmitting accident scene which involves recording of traffic accident 
incidences when they occur by police,notification and locating of the accident reported by the community (witness or victim). 

iROAD is a loosely coupled modular web based software bundle that is built with
free and open source PHP >= 5.3 Web Frameworks. Among the frameworks Involves;

    * Laravel PHP Web Development Framework
    * Angular JS as a scripting language
    * Google Angular Material Design for presentation layer
    * Composer Package manager
    

iROAD Background
----------------
    The iROAD software is developed by the University of Dar es salaam to help reducing accidents and offences occurring on Tanzania's roads 
	through linking of the stakeholders involved in road safety to improve information sharing and dissemination.
	
	The software should serve for the following data use.
	
    * Reduce accidents through prompt reporting of traffic offences 
    * Time serving in dealing with traffic accidents through Notification / Alerts 
    * Appropriateness of reported information related to road safety 
    * Locating accidents using GIS 
    * Tracking/Verification of licenses and cars registration 
    * Raising awareness of road safety to drivers and general public 
    * Facilitate the management of reported road safety cases 
    * Linking the stakeholders involved in road safety to improve information sharing and dissemination 


Key features and purpose of iROAD 2
-----------------------------------
    * Faster response and less greedy on system resources HRIS was conceived from the start 
      to be fast and to favor performance, its based on laravel Framework that uses Symphony and is about 3 
      times faster than ZendFramework 1.10 while taking 2 times less memory.

    * Unlimited flexiblity through customization Whatever your needs are, HRIS will be 
      adaptable. Its customizable capacity makes it entirely configurable, with less 
      required to be done. Its also extensible, based on framework dependency injection 
      and event dispatchers, more modules can be pluged in with simplicity. iROAD is distributed 
      under GNU General Public Licence which does allow modification and extension of existing features.

    * Ease of use through intuitive, user-friendly interfaces Simple and Flexible user interfaces 
      allows performing advanced tasks simply and intuitively, which allows begginers to the system to quickly feel at ease with iROAD

    * Stable and sustainable The system is in-built with self system tests, that ensures shipped 
      system behaves and performs what is needed with guaranteed compatibility between versions

    * Inteoperable Through Web APIs, iROAD can be interoperated by third party applications through the powerful RESTful APIs


Use of iROAD 2: data collection, processing, interpretation, and analysis.
--------------------------------------------------------------------------

iROAD 2 supports the different facets of the information cycle including:

* Collecting data.

* Running quality checks.

* Data access at multiple levels.

* Reporting.

* Making graphs and maps and other forms of analysis.

* Enabling comparison across time (for example, previous months) and space (for example, across facilities and districts).

* See trends (displaying data in time series to see their min and max levels).

As a first step, iROAD 2 serves as a data collection, recording and compilation tool, and all data (be it in numbers or text form) can be entered into it. Data entry can be done in lists of data elements or in customised user defined forms which can be developed to mimic paper based forms in order to ease the process of data entry.

As a next step, iROAD 2 can be used to increase data quality. First, at the point of data entry, a check can be made to see if data falls within acceptable range levels of minimum and maximum values for any particular data element. Such checking, for example, can help to identify typing errors at the time of data entry. Further, user can define various validation rules, and iROAD 2 can run the data through the validation rules to identify violations. These types of checks help to ensure that data entered into the system is of good quality from the start, and can be improved by the people who are most familiar with it.

When data has been entered and verified, iROAD 2 can help to make different kinds of reports. The first kind are the routine reports that can be predefined, so that all those reports that need to be routine generated can be done on a click of a button. Further, iROAD 2 can help in the generation of analytical reports through comparisons of for example indicators across facilities or over time. Graphs, maps, reports and health profiles are among the outputs that iROAD 2 can produce, and these should routinely be produced, analysed, and acted upon by health managers.


Technical background
--------------------


iROAD as a platform
^^^^^^^^^^^^^^^^^^^

iROAD can be perceived as a platform on several levels. First, the application database is designed ground-up with flexibility in mind. Data structures such as data elements, organisation units, forms and user roles can be defined completely freely through the application user interface. This makes it possible for the system to be adapted to a multitude of locale contexts and use-cases. We have seen that iROAD supports most major requirements for routine data capture and analysis emerging in country implementations. It also makes it possible for iROAD to serve as management system for domains such as logistics, labs and finance.

Second, due to the modular design of iROAD it can be extended with additional software modules. These software modules can live side by side with the core modules of iROAD and can be integrated into the iROAD portal and menu system. This is a powerful feature as it makes it possible to extend the system with extra functionality when needed, typically for country specific requirements as earlier pointed out.


Understanding platform independence
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

All computers have an Operating System (OS) to manage it and the programs running it. The operating system serves as the middle layer between the software application, such as iROAD 2, and the hardware, such as the CPU and RAM. iROAD 2 runs on the Java Virtual Machine, and can therefore run on any operating system which supports Java. Platform independence implies that the software application can run on ANY OS - Windows, Linux, Macintosh etc. iROAD 2 is platform independent, and is extremely useful in the context of public health, where multiple operating systems may be in use.

Furthermore, iROAD 2 is also platform independent when it comes to the Database Management System (DBMS). iROAD 2 uses the Hibernate database abstraction framework and is compatible with any DBMS supported by Hibernate, such as PostgreSQL, MySQL, H2, MS SQL Server, Oracle and many more. PostgreSQL is the recommended DBMS for iROAD 2.

Lastly, and perhaps most importantly, since iROAD2 is a browser-based application, the only real requirement to interact with the system is with a web browser. iROAD2 supports most web browsers, although currently either Google Chrome, Mozilla Firefox or Opera are recommended.


Deployment strategies - online vs offline
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

iROAD 2 is a network enabled application and can be accessed over the Internet, a local intranet and as a locally installed system. The deployment alternatives for iROAD 2 are in this chapter defined as i) offline deployment ii) online deployment and iii) hybrid deployment. The meaning and differences will be discussed in the following sections.

Offline Deployment
""""""""""""""""""

An offline deployment implies that multiple standalone offline instances are installed for end users, typically at the district level. The system is maintained primarily by the end users/district health officers who enters data and generate reports from the system running on their local server. The system will also typically be maintained by a national super-user team who pay regular visits to the district deployments. Data is moved upwards in the hierarchy by the end users producing data exchange files which are sent electronically by email or physically by mail or personal travel. (Note that the brief Internet connectivity required for sending emails does not qualify for being defined as online). This style of deployment has the obvious benefit that it works when appropriate Internet connectivity is not available. On the other side there are significant challenges with this style which are described in the following section.

Hardware: Running stand-alone systems requires advanced hardware in terms of servers and reliable power supply to be installed, usually at district level, all over the country. This requires appropriate funding for procurement and plan for long-term maintenance.

Software platform: Local installs implies a significant need for maintenance. From experience, the biggest challenge is viruses and other malware which tend to infect local installations in the long-run. The main reason is that end users utilize memory sticks for transporting data exchange files and documents between private computers, other workstations and the system running the application. Keeping anti-virus software and operating system patches up to date in an offline environment are challenging and bad practices in terms of security are often adopted by end users. The preferred way to overcome this issue is to run a dedicated server for the application where no memory sticks are allowed and use an Linux based operating system which is not as prone for virus infections as MS Windows.

Software application: Being able to distribute new functionality and bug-fixes to the health information software to users are essential for maintenance and improvement of the system. Relying on the end users to perform software upgrades requires extensive training and a high level of competence on their side as upgrading software applications might a technically challenging task. Relying on a national super-user team to maintain the software implies a lot of traveling.

Database maintenance: A prerequisite for an efficient system is that all users enter data with a standardized meta-data set (data elements, forms etc). As with the previous point about software upgrades, distribution of changes to the meta-data set to numerous offline installations requires end user competence if the updates are sent electronically or a well-organized super-user team. Failure to keep the meta-data set synchronized will lead to loss of ability to move data from the districts and/or an inconsistent national database since the data entered for instance at the district level will not be compatible with the data at the national level.

Online deployment
"""""""""""""""""

An online deployment implies that a single instance of the application is set up on a server connected to the Internet. All users (clients) connect to the online central server over the Internet using a web browser. This style of deployment currently benefits from the huge investments in and expansions of mobile networks in developing countries. This makes it possible to access online servers in even the most rural areas using mobile Internet modems (also referred to as dongles).

This online deployment style has huge positive implications for the implementation process and application maintenance compared to the traditional offline standalone style:

Hardware: Hardware requirements on the end-user side are limited to a reasonably modern computer/laptop and Internet connectivity through a fixed line or a mobile modem. There is no need for a specialized server for each user, any Internet enabled computer will be sufficient. A server will be required for online deployments, but since there is only one (or several) servers which need to be procured and maintained, this is significantly simpler (and cheaper) than maintaining many separate servers is disparate locations.

Software platform: The end users only need a web browser to connect to the online server. All popular operating systems today are shipped with a web browser and there is no special requirement on what type or version. This means that if severe problems such as virus infections or software corruption occur one can always resort to re-formatting and installing the computer operating system or obtain a new computer/laptop. The user can continue with data entry where it was left and no data will be lost.

Software application: The central server deployment style means that the application can be upgraded and maintained in a centralized fashion. When new versions of the applications are released with new features and bug-fixes it can be deployed to the single online server. All changes will then be reflected on the client side the next time end users connect over the Internet. This obviously has a huge positive impact for the process of improving the system as new features can be distributed to users immediately, all users will be accessing the same application version, and bugs and issues can be sorted out and deployed on-the-fly.

Database maintenance: Similar to the previous point, changes to the meta-data can be done on the online server in a centralized fashion and will automatically propagate to all clients next time they connect to the server. This effectively removes the vast issues related to maintaining an upgraded and standardized meta-data set related to the traditional offline deployment style. It is extremely convenient for instance during the initial database development phase and during the annual database revision processes as end users will be accessing a consistent and standardized database even when changes occur frequently.

This approach might be problematic in cases where Internet connectivity is volatile or missing in long periods of time. iROAD2 however has certain features which requires Internet connectivity to be available only part of the time for the system to work properly, such as offline data entry and the MyDatamart tool presented in a separate chapter in this guide, which cater to information flow in situations when Internet connectivity may be challenging.

Hybrid deployment
"""""""""""""""""

From the discussion so far one realizes that the online deployment style is favourable over the offline style but requires decent Internet connectivity where it will be used. It is important to notice that the mentioned styles can co-exist in a common deployment. It is perfectly feasible to have online as well as offline deployments within a single country. The general rule would be that districts and facilities should access the system online over the Internet where sufficient Internet connectivity exist, and offline systems should be deployed to districts where this is not the case.

Defining decent Internet connectivity precisely is hard but as a rule of thumb the download speed should be minimum 10 Kbyte/second and accessibility should be minimum 70% of the time.

In this regard mobile Internet modems which can be connected to a computer or laptop and access the mobile network is an extremely capable and feasible solution. Mobile Internet coverage is increasing rapidly all over the world, often provide excellent connectivity at low prices and is a great alternative to local networks and poorly maintained fixed Internet lines. Getting in contact with national mobile network companies regarding post-paid subscriptions and potential large-order benefits can be a wort-while effort. The network coverage for each network operator in the relevant country should be investigated when deciding which deployment approach to opt for as it might differ and cover different parts of the country.

Server hosting
""""""""""""""

The online deployment approach raises the question of where and how to host the server which will run the iROAD 2 application. Typically there are several options:

Internal hosting within the Ministry of Health

Hosting within a government data centre

Hosting through an external hosting company

The main reason for choosing the first option is often political motivation for having physical ownership of the database. This is perceived as important by many in order to own and control the data. There is also a wish to build local capacity for server administration related to sustainability of the project. This is often a donor-driven initiatives as it is perceived as a concrete and helpful mission.

Regarding the second option, some places a government data centre is constructed with a view to promoting and improving the use and accessibility of public data. Another reason is that a proliferation of internal server environments is very resource demanding and it is more effective to establish centralized infrastructure and capacity.

Regarding external hosting there is lately a move towards outsourcing the operation and administration of computer resources to an external provider, where those resources are accessed over the network, popularly referred to as cloud computing or software as a service. Those resources are typically accessed over the Internet using a web browser.

The primary goal for an online server deployment is provide long-term stable and high-performance accessibility to the intended services. When deciding which option to choose for server environment there are many aspects to consider:

Human capacity for server administration and operation. There must be human resources with general skills in server administration and in the specific technologies used for the application providing the services. Examples of such technologies are web servers and database management platforms.

Reliable solutions for automated backups, including local off-server and remote backup.

Stable connectivity and high network bandwidth for traffic to and from the server.

Stable power supply including a backup solution.

Secure environment for the physical server regarding issues such as access, theft and fire.

Presence of a disaster recovery plan. This plan must contain a realistic strategy for making sure that the service will be only suffering short down-times in the events of hardware failures, network downtime and more.

Feasible, powerful and robust hardware.

All of these aspects must be covered in order to create an appropriate hosting environment. The hardware requirement is deliberately put last since there is a clear tendency to give it too much attention.

Looking back at the three main hosting options, experience from implementation missions in developing countries suggests that all of the hosting aspects are rarely present in option one and two at a feasible level. Reaching an acceptable level in all these aspects is challenging in terms of both human resources and money, especially when compared to the cost of option three. It has the benefit that is accommodates the mentioned political aspects and building local capacity for server administration, on the other hand can this be provided for in alternative ways.

Option three - external hosting - has the benefit that it supports all of the mentioned hosting aspects at a very affordable price. Several hosting providers - of virtual servers or software as a service - offer reliable services for running most kinds of applications. Example of such providers are Linode and Amazon Web Services. Administration of such servers happens over a network connection, which most often anyway is the case with local server administration. The physical location of the server in this case becomes irrelevant as that such providers offer services in most parts of the world. This solution is increasingly becoming the standard solution for hosting of application services. The aspect of building local capacity for server administration is compatible with this option since a local ICT team can be tasked with maintaining the externally hosted server, but with not being burdened with worrying about power supply and bandwidth constraints which usually exist outside of major data centres.

An approach for combining the benefits of external hosting with the need for local hosting and physical ownership is to use an external hosting provider for the primary transactional system, while mirroring this server to a locally hosted non-critical server which is used for read-only purposes such as data analysis and accessed over the intranet.