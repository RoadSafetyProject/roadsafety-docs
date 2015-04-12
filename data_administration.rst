..index:: System Settings

System Settings
===============

The data administration module provides a range of functions to ensure that the data stored in the iROAD2 database is
integral and that the database performance is optimised. These functions should be executed on a regular basis by a
data administrator to ensure that the quality of the data stored is optimal.

Data browser
============

The data browser maintenance and analysis module which allows the user to produce a summary of the data contained
in the iROAD2 database. The summary view provides a count of data elements which have been entered at the selected
organisation unit as well as its descendants. Raw data for all data elements for a range of time periods and a given
organisational unit can be browsed and exported to Excel, CSV, or PDF formats. There are four modes of the data
browser, which determine how the data is summarized

* Data sets
* Data element groups
* Organisational unit groups
* Organisational units

Each of these options can be accessed by selecting the desired option from "Browse by" drop-down menu.
In order to produce a summary of submitted data for a given period and grouped by data sets, the user should follow
this procedure. Begin by selecting a given periodicity type (e.g. Weekly, monthly, yearly, etc) and then a "From date"
and "To date". (e.g. January 2009 to March 2009). Select the type of summary to be produced (e.g. Dataset) from the
"Browse by" drop-down menu. Click the "Browse" button to view the summary.

.. _data_elements:
.. figure::  images/dataelements.png
   :align:   center
   
A summary of the number of data element values that have been submitted over the user selected time period is shown
below.

Data integrity
==============
iROAD2 can perform a wide range of data integrity checks on the data contained in the database. Identifying and
correcting data integrity issues is extremely important for ensuring that the data used for analysis purposes is valid.
Each of the data integrity checks that are performed by the system will be described, along with general procedures
that can be performed to resolve these issues.

Data elements without data set
------------------------------

Each data element must be assigned to a data set. Values for data elements will not be able to be entered into the system
if a data element is not assigned to a data set. Choose Maintenance->Datasets->Edit from the main menu and then add
the "orphaned" data element to the appropriate data set.

Data elements without groups
----------------------------

Some Data Elements have been allocated to several Data Element Groups. This is currently not allowed, because it will
result in duplication of linked data records in the analytics record sets that provide aggregated data. Go to Maintenance
-> Data Element Groups to review each Data Element identified and remove the incorrect Group allocations.

Data elements violating exclusive group sets
--------------------------------------------

Some data elements have been allocated to several data element groups that are members of the same data element
group set. All group sets in iROAD2 are defined as exclusive, which means that a data element can only be allocated
to one data element group within that group set. Go to Maintenance -> Data elements and indicators ->Data element
groups to review each data element identified in the integrity check. Either remove the data element from all groups
except the one that it should be allocated to, or see if one of the groups should be placed in a different group set.

Data elements in data set but not in form or sections
-----------------------------------------------------
Data elements have been assigned to a data set, but have not been assigned to any sections of the data set forms. All
data sets which use section forms, should generally have all data elements in the data set assigned to exactly one section
of the dataset.

Data elements assigned to data sets with different period types
---------------------------------------------------------------
Data elements should not be assigned to two separate data sets whose period types differ. The recommended approach
would be to create two separate data elements (for instance a monthly and yearly data element) and assign these to
respective datasets.

Data sets not assigned to organisation units
--------------------------------------------
All data sets should be assigned to at least one organisation unit.

Sections with invalid category combinations
-------------------------------------------
Data sets which use section forms should only have a single category combination within each section. This violation
could result from assigning a data element to a section, but then changing the category combination of this data element
at a later point in time.

Indicators with identical formulas
----------------------------------
Although this rule will not affect data quality, it generally does not make sense to have two indicators with the exact
same definition. Review the identified indicators and their formulas and delete or modify any indicator that appears
to be the duplicate.

Indicators without groups
-------------------------
All data elements and indicators must be assigned to at least one group, so these Indicators need to be allocated to their
correct Data Element and Indicator Group. From the main menu, go to Data elements/Indicators -> Indicator Groups,
and allocate each of the `Orphaned` indicators to its correct group.

Invalid indicator numerators
----------------------------
Violations of this rule may be caused by an incorrect reference to a deleted or modified data element. Review the
indicator and make corrections to the numerator definition.

Invalid indicator denominators
------------------------------
Violations of this rule may be caused by an incorrect reference to a deleted or modified data element. Review the
indicator and make corrections to the denominator definition.

Indicators violating exclusive group sets
-----------------------------------------
Some indicators have been allocated to several indicator groups that are members of the same indicator group set. All
group sets in iROAD2 are defined as exclusive, which means that an indicator can only be allocated to one indicator
group within that group set. Go to Maintenance -> Data elements and indicators ->Indicator groups to review each
indicator identified in the integrity check. Either remove the indicator from all groups except the one that it should be
allocated to, or see if one of the groups should be placed in a different group set.

Duplicate periods
-----------------
If periods have been imported from external applications, it may be possible that some periods will be duplicated. If
you have any periods which appear to be duplicated here, you will need to resolve these directly in the iROAD2 database.
All data which has been assigned to the duplicated period, should be moved to the correct period, and the duplicate
period should be removed.

Organisation units with cyclic references
-----------------------------------------

Organisation units cannot be both parent and children of each other, directly nor indirectly. If this situation occurs, you
will need to resolve the cyclic reference directly in the iROAD2 datrabase in the "organisationunit" table, by reassigning
the "parentid" field of the organisation units.

Orphaned organisation units
----------------------------
All organisation units must exist within the organisation unit hierarchy. Go to Organisation- units >Hierarchy
Operations and move the offending organisation unit into the proper position in the hierarchy.

Organisation units without groups
---------------------------------
All organisation units must be allocated to at least one group. The problem might either be that you have not defined any
compulsory OrgUnit Group Set at all, or that there are violations of the compulsory rule for some OrgUnits . NOTE: If
you have defined no compulsory OrgUnit Group Sets, then you must first define them by going to Organisation units>Organisation unit group sets and define at least one compulsory Group Set (the group set 'Type' are nearly universally
relevant). If you have the relevant group sets, go to Maintenance -> OrgUnit Groups to review each OrgUnit identified
and add the relevant Group allocation.


