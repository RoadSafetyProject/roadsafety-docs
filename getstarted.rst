.. _getstarted:


Road Safety Management Information System (iROAD) is a software that intends to improve Management of Road Safety in Tanzania.

iROAD enables Car registration and use validity which involves verification of the car registration, 
driver and road license validity by police, customs, or TRA; Capturing, storage and use of traffic 
offence incidents which involves recording of traffic offence incidences when they occur by police or 
reported by the community (witness or victim), notification and-or educating of the offender by police 
about the offence(s) committed and tracking of the payment of fines or court decisions that result from 
the offence(s); Recording and transmitting accident scene which involves recording of traffic accident 
incidences when they occur by police,notification and locating of the accident reported by the community (witness or victim). 

iROAD is a loosely coupled modular web based software bundle that is built with
free and open source PHP >= 5.3 Web Frameworks. Among the frameworks Involves

    * Laravel PHP Web Development Framework
    * Angular JS as a scripting language
    * Google Angular Material Design for presentation layer
    * Composer Package manager
    
.. index:: Why Would you want to choose iROAD

Why Would you want to choose iROAD
===================================
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

.. index:: Introduction to iROAD

Introduction to iROAD
======================

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


The System Target Users
-----------------------

The system provides different user access levels.  Which should include, but not limited to,
 
    * Officers of Police Force 
	* Officers of Fire and Rescue Force
	* Officers of Hospitals 
	* Officers of Insurance company
	* Officers of Police Force 
    * Officers of TRA, SUMATRA, TANROADS, RITA, NIDA
	* Officers of relevant ministries including, but not limited to, Ministry of Home Affairs and Ministry of Transport 
	* Community users


.. index:: System Administration

System Administration
---------------------

    Users with System administrative priviledge(i.e Major Stakeholders) can customize the system by providing specific information to be used throughout the system.
	Also these priviledged users can control the access of data in different parts of the system and other system customizations that affect the system at large.

	
.. index:: Accessing the System

Accessing the System
--------------------

    System is in-built with secured Authentication and Authorization system that requires users to be authenticated to 
    use any service that requires a user to be loged in and require user to be authorised as cleared to use some of 
    priviledged system services, such as right to control data to be collected.

Managing System Reports
-------------------------

    System uses Report module to produuce different reports on drivers,vehicles,offences and accidents information. 

.. index:: Modules and Features

Modules and Features
--------------------

    iROAD Consists of Several modules designed to collect, validate, report and analyse road related information, the modules consist

        * User Module to manage system users.
		* Drivers Module to manage drivers information(i.e registering drivers to TRA and etc).
		* Motor Vehicle module to track information on all vehicles, this includes vehicle's insurance, inspections,offences and accidents the vehicle is involved if any and so many others.)
        * Offence Module to Manage and track road offences.
		* Accident Module to manage and track all road accidents.
		* Organisationunits Management Creates and manages organisation units, it's properties as in ownership, type, and other attributes, like level in a hierarchy, etc.
        * Data Quality Management Creates and manages validation constraints that are used to test and ensure quality data is being collected
        

.. index:: Properties of iROAD

Properties of iROAD
-------------------

    * Web and Mobile enabled
    * Platform independent
    * Runs on all major web browsers
    * Runs on most relational databases
    * Licenced under open source licence terms
    * Works Off-line
    * Loosely coupled with Bundle/Modular approach
    * Interoperable
    * Internationalized