..index:: Using GIS

Using GIS
=========

GIS module overview
===================
You can access the GIS module from the Services -> GIS link in the top menu. The picture below shows the GIS viewport.

.. _gis_main:
.. figure::  images/gis_main.png
   :align:   center
   
In the top right corner there is a panel called "Layer overview". If you are online you will see Google Streets and Google Hybrid which can be used as background maps/layers. Switch between the two of them by checking the checkbox. By unchecking the box you can hide the background completely. If you want to see the background, but with reduced opacity, you can set the visibility to something lower than 100% in the numberbox to the right. The final four layers are the vector layers which the user has at his disposal for thematic mapping (explained in the next section). The panels below hold the map legends when you create a thematic map. A legend explains the link between values and colors on your map.

Lets take a look at the map toolbar. The four icons from the left represent the mentioned vector layers and this is the starting point of the GIS application. Further to the right we have "Favorites": Save your maps to easily restore them later. Saving a map as a favorite also gives you the opportunity of sharing it with other users as an interpretation or put it on the dashboard. "Legend": Create you own legend sets to ensure meaningful maps. "Download": Export the maps as a PNG image. "Share": Share your favorites as map interpretations with other users.

In the top right corner of the map viewport you find four buttons: "Zoom in", "zoom out", "zoom to visible extent" (automatically adjusts the zoom level and map center position to put the data on your map in focus) and "measure distances".

The current longitude/latitude position of the mouse cursor is displayed in the bottom right corner of the map viewport.


Thematic mapping
================
This section describes the four vector layers which the user has at his disposal for thematic mapping: "Facility layer", "Boundary layer" and "Thematic layer" 1-4.

.. _gis_facility_layer:
.. figure::  images/gis_facility_layer.png
   :align:   center
   
This layer displays icons that represent facilities based on the facility type. Polygons will not show up on the map, so make sure to select an organisation unit level that has facilities. Click an icon on the map to open the context menu with two options. "Show information sheet" provides you with data for several data elements for this organisation unit. The data element group and period type are "system settings" called "Infrastructural data elements" and "Infrastructural period type". The second option in the context menu is "Relocate" and lets you graphically move the organisation unit to a different location. The new coordinate will be stored permanently. Browser cache must be deleted to see the change if you reload the page.

In the "Edit layer" window will find "surrounding areas" in addition to group set, level and parent. This lets you draw a circle around each facility with a desired radius in kilometers.

Boundary layer
--------------

.. _gis_boundary_layer:
.. figure::  images/gis_boundary_layer.png
   :align:   center
   
The purpose of the boundary layer is to display the boundaries/coordinates in the system. No data will be shown. This layer is useful if you are offline and thus have no background map. Click the boundary/globe icon on the toolbar and select "Edit layer". You can select the organisation units you want to show on the map by selecting a level and a parent. That means "show all organisations units at this level that are children of this parent". When there are visible organisation units on the map, you can easily navigate up and down in the hierarchy without using the level/parent user interface. By clicking one of the organisation units a context menu will open, then select "drill down" or "float up". The drill down option will be disabled if you are already on the lowest level or if there are no coordinates available on the level below. Vice versa goes for floating up.

The layer menu also offers to put on labels and to locate an organisation unit in the map.

The final option in the layer menu is "Close". This completely resets the layer content, the edit layer form and the legend panel.

Thematic layer 1-4
------------------

.. _gis_thematic_mapping:
.. figure::  images/gis_thematic_mapping.png
   :align:   center
   
The four thematic layer panels let you use your data for thematic mapping. All you need to do is selecting your desired combination of indicator/dataelement, period and map combination. Then the organisation unit level and parent to define the boundaries. If your database has coordinates and aggregated data values for these organisation units they will appear on the map. Note that the iROAD2 data mart must be run in order to have aggregated values available.

You may choose between legend types: automatic and predefined. Automatic means that the application will create a legend set for you based on your what method, number of classes, low color and high color you select. Method alludes to the size of the legend classes. Set to Equal intervals they will be highest map value "-" lowest map value / number of classes. Set to Equal group count the legend creator will try to distribute the organisation units evenly. The legend will appear as an even gradation from the start color to the end color. Predefined legend sets are described in Section 17.3.2, Create predefined legend sets.

Low radius and high radius only have effect on points (facilities) and decides the circle radius for points with the lowest and highest value.

Thematic layer 1-4 menu have a "Filter" option in addition to the boundary layer menu options. It lets you apply value filters to the organisation units on the map. The filter is removed when you close the filter window.

Event layer
-----------

.. _gis_event_layer:
.. figure::  images/gis_event_layer.png
   :align:   center
 
The purpose of the event layer is to display the geographical location of events registered in the iROAD 2 tracker. This layer enables you to drill down from the aggregated data displayed in the thematic layers to the underlying individual events or cases.

To work with this layer, click the event layer icon on the map toolbar and select "Edit layer". Select a program and then select a program stage. If there is only one stage available for the selected program, the stage will be automatically selected. A list of data elements and attributes will appear in the "Available data elements" panel. You are free to select and use any data element or attribute from this list as part of your query. To select you can either double-click a data element or (multi) select and use the single-arrow downward button. The double-arrow button will select all data elements in the list. All selected data elements will get their own row in the "Selected data elements". You can also use an element multiple times in your query by clicking the + button. For data elements of type text you will get two choices: "Contains" implies that the query will match all values which contains your search value, and "Is exact" implies that only values which is completely identical to your search query will be returned. For data elements of type option set, you can select any of the options from the drop down box by using the down-wards arrow or by start typing directly in the box to filter for options.

The event layer also requires you to select the time span for when the events took place using the "start date" and "end date" date pickers under the "Periods" section, as well as the organisation units to include in the query under the "Organisation units" section.

To get information for an event you can simply click on it. This will open a dialog which displays all available information for that event.

The layer menu also offers to put labels on the map and to close the layer, which completely resets the layer content.

Tools
=====
This section describes the available GIS tools.  
      
Favorite maps
-------------

Click the "Favorites" button on the toolbar to open the "Manage favorites" window. To add a new favorite, click the "Add new" button. A new window opens. Enter a name and click the "Create" button. You will find your new favorite in the list.

All favorites have four action buttons on the right hand side. Grey: Edit favorite name. Green: Save current map to this favorite (overwrite). Yellow: Add this favorite to dashboard. Red: Delete this favorite.

You can search for favorites in the textfield above the favorites. The list will be filtered on every character that is entered. Click the "next" and "prev" buttons in the bottom right corner to navigate between pages.

Create predefined legend sets
-----------------------------
Click the "Legend" button on the map toolbar. To create a new set click the "Add new" button. Example usage (vaccination coverage): Firstly, give the legend set a name. Then create the legends you want in your legend set. The first one could be "Low bad" (name), 0 (start value), 50 (end value), red (color). Click "Add legend" and appears in the list below. Then create "Medium" / 50 / 80 / yellow, "High good" / 80 / 100 / green and finally "Too high" / 100 / 10000 / grey. Now, click the "Create" button in the bottom right corner. If your legend set has overlapping legends (e.g. 0-50 and 40-80) you will not be allowed to proceed. If your legend set has a gap between the legends (e.g. 0-50 and 60-80) you will get a warning, but are allowed to proceed.

NOTE! Continuous legends are supposed to end and start on the same value, e.g. 0-50 and 50-80. This will automatically be taken care of by the application. Do not try to do this yourself by setting legends to e.g. 0-50 and 51-80. This will cause a usually unwanted gap in your legend set.

You can assign a legend set to an indicator or a data element in the Indicator/Data element module. This legend set will then be automatically selected when such an indicator/data element is selected in the GIS.

Download map as image
---------------------
Click the "Download" button on the map toolbar. Enter a name in the textfield and click "Download". The browser will download a PNG image. If the toolbar "Download" button is disabled you need to create a map first.

Share map interpretation
-------------------------
Open a favorite or save a new map as a favorite. Then click the "Share" button on the map toolbar. Type in your interpretation and click "Share".

Embed maps in any web page
--------------------------
Certain analysis-related resources in iROAD, like pivot tables, charts and maps, can be embeded in any web page by using a plugin. If you have created a map in the GIS app you will get the plugin configuration for this map by clicking the "Share" button the toolbar and then "Embed as plugin". You will find more information about the plugins in the web api chapter.

Analysis integration
--------------------
The analysis apps in iROAD 2 are completely integrated, so you can easily switch between pivot table, chart and map visualization of your data. When you have made a map you can click e.g. "Chart" in the top right corner and then select "Open this map as chart".

