..index:: Settings

System Settings
===============

The settings module provides a set of application configuration options. There are two main groups of settings: the
system settings apply to the whole system and all its users while the user settings apply to the environment of the
currently logged in user. The system settings can be accessed from the maintenance menu, settings module. The user
settings can be accessed under the profile menu, settings page.

System settings
===============

The system settings section provides general configuration options and options specifically for appearance and email.

General settings
----------------

*  Cache strategy: Decides for how long reports and responses related to analysis should be cached. 

If you are using the scheduled, nightly data mart tasks it makes sense to put this on "Cache until 6 AM tomorrow". This is because
we know that data in reports change at that time, and you can safely cache data up to the moment when the data mart
is updated. If you are loading data continuously into the datamart you should set it to "No cache". If you load data
very infrequently into data mart you should consider setting it to "Cache for two weeks".

*  Maximum number of analytics records: This number can be increased to provide more records from the analytics.

The default is 50,000 and can be increased

Warning::
You should be exceedingly careful when increasing the maximum number of analytics records, for instance to Unlimited. This could result in severe server instability, due to clients requesting large amounts of data
from the system.

*  Number of database server CPUs:

The number of CPU cores of your database server can be configured as a system setting. 
This allows the system to perform optimally when the database is hosted on a different server than the
application server, as the analytics engine scales linearly on the number of available cores.

*  Infrastructural data elements: 

This setting defines a data element group where the member data elements should describe data about the infrastructure of organisation units. 
Examples of such infrastructural data elements could be population, doctors, beds, Internet connectivity and climate. This infrastructural data can currently be viewed in the
GIS module in the facility information sheet.

*  Infrastructural period type: 

Sets the frequency for which the data elements in the infrastructural data elements group
are captured. This will typically be yearly. When viewing the infrastructural data you will be able to select the time
period of the data source.

*  Feedback recipients: 

This setting defines a user group where the members will receive all messages being sent
through the function for writing feedback in the dashboard module. This will typically be members of the super user
team who are able to support and answer questions coming from end-users.

*  Maximum offline organisation unit levels: 

This setting defines how many levels in the organisation unit hierarchy
will be available offline in the organisation unit tree widget. Under normal circumstances you can leaves this on the
lowest level, which is default behavior. Setting it to a higher level might be useful in order to reduce initial load time
in cases where you have a large number of organisation units, typically more than 30 000.

* System notifications email address: 

An email address can be specified to receive system notifications. Notifications
about failures in processes such as analytics table generation will be sent here. This is useful for application
monitoring.

* Data analysis std dev factor: 

Sets the number of standard deviations for use in the outlier analysis performed on
the captured data in the data entry module. The default value is 2; a high value will catch less outlier values than
a low value.

* Days after period end to qualify for timely data submission: 

Sets the number of days after the end of a period in
which a data entry form must be marked as complete in order to be considered timely. This affects the "reporting rate" tool in the reporting module which lists forms marked as complete as well as marked as complete in time.
The default value is 15.

* Phone number area code:

The area code for the area in which your deployment is located. Used for sending and
receiving SMS.Typically, this would be a country code, for instance , +260 , which is the country code for Zambia.

*  Help page link:

A URL can be provided for an alternative help source. This defines the URL which users will see
when selecting Profile->Help.

* Google Analytics (Universal Analytics) Key: 

Set your Google UA key here to provide analytics for your iROAD 2
instance. Most places are covered, but it will not be provided for custom apps. Read more about Google Analytics
at http://google.com/analytics .

* Enable multi-organisation unit forms: 

Enable support for entering data forms for multiple organisation units at the same time, in data entry, click on the parent organisation unit for the children that you want to enter data for, and
the dataset list will include datasets that are assigned to the children of that parent.

* Omit indicator values with zero numerator value in data mart:

Defines whether aggregated indicator values with
zero as the numerator value should be written to the indicator data mart table. Having such values written is required
for instance when connecting Excel pivot tables to the data mart as Excel will need the numerator data to correctly
aggregate up in the organisation unit hierarchy. If third-party tools like Excel are not used with the application this
will reduce the total number of values written to the data mart (which again will improve performance) and could
safely be set to omit.

* Put analytics in maintenance mode: 

Puts the analytics engine / Web API resource in maintenance mode, implying
that 503 Service Unavailable will be returned for all requests. This is useful when you need to perform maintenance
on the server like rebuilding indexes while the server is running in production, in order to reduce load and more
efficiently carry out the maintenance.

System appearance settings
--------------------------

*  Application title: Sets the application title on the top menu.

*  Application introduction: Sets an introduction of the system which will be visible on the top-left part of the login page.

*  Application notification: Sets a notification which should be displayed to users. Will be visible on the front page under the login area.

*  Application footer: Sets a text in the footer area of the login page.

*  Style: Sets the style / look-and-feel of the system. The corresponding user style setting overrides this.

*  Start page: Sets page / module which the user will be redirected to after logging in. The dashboard module is the recommended start module.

*  Flag: Sets the flag which is displayed in the left menu of the dashboard module.

*  Require authority to add to view object lists: 

Will hide menu and index page items / links to lists of objects if the
current user does not have the authority to create the type of objects (privately or publicly).


Email settings
--------------

*  Host name: Refers to the host name of the SMTP server. For instance when using Google SMTP services this should be smtp.gmail.com.

*  Port: The port to connect to the SMTP server.

*  User name: The user name of the user account with the SMTP server. For instance mail@iROAD2.org.

*  Password: The password of the user account with the SMTP server.

*  TLS: Refers to whether the SMPT server requires TLS for connections.


Access settings
---------------

* Self registration account user role: 

Defines which user role should be given to self-registered user accounts. To
enable self-registration of users, select any user role from the list. To disable it, select "Do not allow self registration".
When enabled, a link to the self-registration form will be displayed on the login page.

* Do not require recaptcha for self registration: 

Whether or not to use reCAPTCHA for user registration.

* Self registration account organisation unit: 

Defines which organisation unit should be associated with self-registered users. Any organisation unit must be selected in order to enable self registration.

* Enable user account recovery:

Defines whether users are allowed to restore the password of their account if they
forgotten it. When enabled, a link to the account recovery form will be displayed on the front page. User account
recovery requires that you have configured email settings (SMTP).

* Enable user account invite: 

Defines user account invites can be sent. Account invites let you invite new users to create their own accounts by sending an email invitation.

* Allow users to grant own user roles: 

Defines whether users should be allowed to grant the user roles they are granted themselves to others.

* Users must belong to a group controlled by the user manager:

This allows user groups to play a role in user management. When checked, user A can manage user B only if user B belongs to a user group to which user A has read/write access. When user A creates a new user, she or he must assign the new user to such a user group.

* Require user account password change:

Require that users change their password every 3,6,12 months. Please note that for 2.14 release, they will have to login through the desktop to change passwords.

* OpenID provider: Defines the OpenId provider.

* OpenID provider label: Defines the label to display for the specified OpenID provider.

Calendar settings
-----------------

* Calendar: 

Defines which calendar system should be used throughout the system.
There are currently eight calendar systems which are supported, namely Coptic, Ethiopic, Gregorian, Julian, Islamic,
ISO, Nepal and Thai. Note that this is a system wide setting. It is not possible to have multiple calendars within a
single iROAD2 instance.

* Date format: 

Defines which date format should be used throughout the system.


Synchronization settings
------------------------

* Remote server URL: The URL of the remote server running iROAD 2 to upload data values to.

Use of SSL/HTTPS is recommended since username and password is sent with the request (using basic authentication). The system will
attempt to synchronize data once every minute. Note that you must enable data synch from Data administration >
Scheduling.

* Remote server username:

The username of the iROAD 2 user account on the remote server to use for data synchronization.

* Remote server password: 

The password of the iROAD 2 user account on the remote server. The password will be stored encrypted.


Remote access settings
----------------------

* CORS whitelist: A list of domains to acccept cross-origin requests for resources. CORS is a mechanism that allows resources to be requested from another domain. This means e.,g. that you can make requests to the iROAD 2 Web API from a web page or portal living on another domain than the iROAD 2 instance.

