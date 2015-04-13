..index:: Pivot Table overview

Pivot Table overview
====================
The pivot table app enables users to create pivot tables, using all available data dimensions in iROAD 2. A pivot table is a dynamic tool for data analysis which lets you quickly summarize and arrange data according to its dimensions. Examples of data dimensions in iROAD 2 are data elements (explaining what the data means), periods (representing the time aspect) and the organisational hierarchy (representing the geographical location of the data). From these dimensions you can freely select dimension items to include in the pivot table. Additional dimensions can be created in iROAD2, using the group set functionality, to allow for different aggregation pathways, such as aggregation by "Partner" or facility type.

A pivot table can arrange data dimensions on columns, rows, and as filters. When you place a data dimension on columns, the pivot table will display one column per dimension item. If you place multiple data dimensions on columns, the pivot table will display one column for all combinations of the items in the selected dimensions. When you place a data dimension on rows, the pivot table will display one row per dimension item in a similar fashion. The dimensions you select as filters will not be included in the pivot table, but will aggregate and filter the table data based on the selected filter items.

The workflow for creating a simple pivot table is:

* Select dimension items in the left menu, for instance a few data elements or indicators.

* Click "Layout" on the top menu and arrange the data dimensions as columns, rows, and filters. You can leave the selection as it is if desired.

* Click "Update".

Based on the demo database, a pivot table approximately as below will be displayed. Notice how indicators are listed on columns and periods as rows.

.. _basic_pivot:
.. figure::  images/basic_pivot.png
   :align:   center
   
Selecting dimension items
=========================
The left menu will list sections for all available data dimensions. From each section you can select any number of dimension items. As an example, you can open the section for data elements and select any number of data elements from the available list. You can select an item by marking it and clicking on the arrow in the section header or simply double-clicking on the item. Before you can use a data dimension in your pivot table you must at least select one dimension item. If you arrange a dimension as columns or rows but do not select any dimension items, the dimension will be ignored.

For the indicator and data element dimensions you must first select one or all groups from the group list. You can then select data elements from the available items list.

For the period dimension you can choose between using fixed periods or relative periods. An example of a fixed period is "January 2012". To select fixed periods start by selecting a period type from the period type list. You can then select periods from the list of available periods. Relative periods are periods relative to the current date. Examples of relative periods are "Last month", "Last 12 months", "Last 5 years". Relative periods can be selected by ticking the checkboxes next to each period. The main advantage of using relative periods is that when you save a pivot table favorite, it will stay updated with the latest data as time goes by without the need for constantly updating it.

For the organisation unit dimension you can select any number of organisation units from the hierarchy. To select all organisation units below a specific parent organisation unit, right click and click "Select all children". To manually select multiple organisation units, click and hold the Ctrl button while clicking on organisation units. You can tick "User organisation unit", "User organisation unit children" or "User organisation unit grand children" in order to dynamically insert the organisation unit or units associated with your user account. This is useful when you save a pivot table favorite and want to share it with other users, as the organisation units linked with the other user's account will be used when viewing the favorite.


.. _period_dimension:
.. figure::  images/period_dimension.png
   :align:   center
   
Arranging the table layout
==========================
After selecting data dimensions it is time to arrange your pivot table. Click "Layout" in the top menu to open the layout screen. In this screen you can position your data dimensions as table columns, rows or filters by clicking and dragging the dimensions from the dimensions list to the respective column, row and filter lists. You can set any number of dimensions in any of the lists. For instance, you can click on "Organisation units" and drag it to the row list in order to position the organisation unit dimension as table rows. Note that indicators, data elements and data set reporting rates are part of the common "Data" dimension and will be displayed together in the pivot table. For instance, after selecting indicators and data elements in the left menu, you can drag "Data" from the available dimensions list to the row dimension list in order to arrange them as rows in the pivot table.

.. _table_layout:
.. figure::  images/table_layout.png
   :align:   center
   
After you have set up your pivot table you can click "Update" to render your pivot table, or click "Hide" to hide the layout screen without any changes taking effect. Since we in our example have selected both the period and organisation unit dimension as rows, the pivot table will generate all combinations of the items in these dimensions and produce a table like this:

.. _pivot_rows:
.. figure::  images/pivot_rows.png
   :align:   center
 
Using table options
===================

Several table options are available when working with a pivot table. Open the options screen by clicking on "Options" in the top menu. The following options are available:

* Show totals: Display total values in the table for each row and column, as well as a grand total for all values in the table.

* Show sub-totals: Display subtotals in the table for each dimension. In the screenshot above, notice how subtotals are generated for each of the periods in the period dimension. Note that subtotals will be hidden for columns or rows if there is only one selected dimension, as the values in that case are equal to the subtotals.

* Hide empty rows: Hides empty rows from the table, which is useful when looking at large tables where a big part of the dimension items do not have data in order to keep the table more readable.

* Show hierarchy: Shows the name of all ancestors for organisation units, e.g. "Sierra Leone / Bombali / Tamabaka / Sanya CHP" for Sanya CHP. The organisation units are then sorted alphabetically which will order the organisation units perfectly according to the hierarchy.

* Display density: Controls the size of the cells in the table. Can be set to "comfortable", "normal" and "compact". The "compact" option is handy in order to fit large tables into the browser screen.

* Font size: Controls the size of the table text font. Can be set to "large", "normal" and "small".

* Digit group separator: Controls which character to separate groups of digits or "thousands". Can be set to "comma", "space" and "none".

* Legend set: Shows a color indicator next to the values. Currently the GIS legend sets are being used.

Creating a favorite
===================
When you have set up a pivot table it is convenient to save it as a favorite. To do so, click "Favorites" on the top menu, click "Add new", give the favorite a descriptive name and click "Create". You can search for favorites through the search input field at the top. To load an existing favorite, simply click the name of the favorite in the list.

To rename a favorite, click the grey "Rename" icon next to the favorite in the list, change the name and click "Update". To overwrite an existing favorite with the current pivot table, click the green "Overwrite" icon. To share a favorite with everyone or a user group, click the blue "Share" icon. To delete a favorite, click the red "Delete" icon.

.. _pivot_favorites:
.. figure::  images/pivot_favorites.png
   :align:   center

Analysis integration
====================
The analysis apps in iROAD 2 are completely integrated, so you can easily switch between pivot table, chart and map visualization of your data. When you have made a pivot table you can click e.g. "Chart" in the top right corner and then select "Open this table as chart".

.. _pivot_integration:
.. figure::  images/pivot_integration.png
   :align:   center

If you just want to visualize a small part of your pivot table as a chart, you can click directly on a value in the table instead. A menu will appear. If you mouse hover the "Open selection as chart" option you can see that some of the dimension headers in the table are highlighted, indicating what data will be visualized as a chart.

.. _pivot_integration_table:
.. figure::  images/pivot_integration_table.png
   :align:   center

Downloading data
================
You can download the data in the current pivot table by clicking on "Download" in the top menu. The data can be downloaded in MS Excel and CSV format. The data table will have one column per dimension and contain names of the dimension items. You can easily create a pivot table in Microsoft Excel from the downloaded Excel file by clicking on "pivot table" in the top panel, then clicking on "create pivot table", then marking the data range in the spreadsheet before clicking "OK".

Data can also be downloaded in JSON and XML format. The data format is specified in the Web API chapter under the "Analytics" section. The data document will use identifiers of the dimension items and will be opened in a new browser window in order to reveal the URL of the request to the Web API in the address bar. This will be useful for developers of apps and other client modules based on the iROAD 2 Web API.

Sharing interpretations
=======================
For certain analysis-related resources in iROAD, like pivot tables, charts and maps, one can share a data interpretation. An interpretation is simply a link to the relevant resource together with a text expressing some insight about the data. If you want to share a pivot table interpretation you need to first save the table you want to share as a favorite. Then, without making any changes to the table, click the "Share" button the toolbar. A window will open up and this is where you write your interpretation. When you are done, click share button in the bottom right corner of the window. The window will close automatically and if the interpretation was shared successfully you will find a notification on the bottom toolbar.

Embed tables in any web page
============================
Certain analysis-related resources in iROAD, like pivot tables, charts and maps, can be embeded in any web page by using a plugin. If you have created a table in the Pivot Table app you will get the plugin configuration for this table by clicking the "Share" button the toolbar and then "Embed as plugin". You will find more information about the plugins in the web api chapter.

Constraints
===========
When selecting and arranging dimensions there are a few constraints that apply. All of these constraints are validated and the pivot table module will provide feedback if any constraint is violated.

* At least one dimension must be selected on columns or rows.

* At least one period must be included in the pivot table.

* Data element group sets and reporting rates cannot appear in the same pivot table.

* A table cannot contain more than the maximum number of analytics records which have been specified through the system settings. The maximum number of records could also be constrained by the maximum RAM which is available to your browser. Considering making more smaller tables, instead of one table which displays all of your data elements and indicators together.

