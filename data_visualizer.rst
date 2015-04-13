..index:: Data Visualizer overview

Data Visualizer overview
========================
The data visualizer module enables users to easily create dynamic data analysis and visualizations through charts and data tables. You can freely select content (like indicators, periods and organisation units) for your analysis. This module can be accessed by going to "Services - Data Visualizer" in the main menu. The image below shows the viewport of the module. For a quick start:

#. Look under the "Indicator" heading and select an indicator group from the list of groups.

#. Look under "Available indicators" and select a few indicators from the list by double-clicking on them.

#. Click "Update" in the top bar and see the chart unfold.

The data visualizer is designed firstly to be easy-to-use - you can simply select the indicators, data elements, periods and organisation units you want to include and click "Update" to get your visualization. Secondly it is designed to be fast and work well over poor Internet connections - charts are generated in the web browser and very little data is transferred over the Internet.

.. _column_chart:
.. figure::  images/column_chart.png
   :align:   center
   
Selecting chart type
====================

The visualizer module provides seven different chart types, each with different characteristics. You can select the type of your chart by clicking on one of the icons in top left bar titled "Chart type".

#. Column chart: Chart which displays information as vertical rectangular columns with lengths proportional to the values they represent. Useful e.g. for comparing performance of different districts.

#. Stacked column chart: Chart with vertical rectangular columns where bars representing multiple categories are stacked on top of each other. Useful e.g. for displaying trends or sums of related data elements.

#. Bar chart: Same as column chart, only with horizontal bars.

#. Stacked bar chart: Same as stacked column chart, only with horizontal bars.

#. Line chart: Graph which displays information as a series of points connected by straight lines. Also referred to as time series. Useful e.g. to visualize trends in indicator data over multiple time periods.

#. Area chart: Chart which is based on line chart, with the space between the axis and the line filled with colors and the lines stacked on top of each other. Useful for comparing the trends of related indicators.

#. Pie chart: Circular chart divided into sectors (or slices). Useful e.g. to visualize the proportion of data for individual data elements compared to the total sum of all data elements in the chart.

#. Radar chart: Displaying multivariate data on axes starting from the same point. Also known as spider chart.

 
Selecting series, category and filter
=====================================

This section lets you define which dimension of the data you want to appear as series, category and filter. This asks for a closer explanation. Dimension in this regard refers to the elements which describe the data values in the system. We have three main dimensions in the system:

#. Data: Includes data elements, indicators and datasets (reporting rates), describing the phenomena or event of the data.

#. Periods: Describes when the event took place.

#. Organisation units: Describes where the event took place.

The visualization module lets you use these dimensions completely flexible in terms of appearing as series, categories and filter. Understanding these concepts is most easily done by looking at the screenshot from the opening page below:

.. _series_category_filter:
.. figure::  images/series_category_filter.png
   :align:   center

More formally this can be described as following:

#. Series: A series is a set of continuous, related elements (e.g. periods or data elements) which you want to visualize in order to emphasize trends or relations in its data.

#. Categories: A category is a set of elements (e.g. indicators or organisation units) for which you want to compare its data.

#. Filter: Since most charts are two-dimensional, a filter must be used on the third dimension in order to use only a single element for the chart to become meaningful.

Selecting indicators and data elements
======================================

The visualizer module can display any number of indicators and data elements in a chart and data table. Both indicators and data elements can be selected and appear together in the same chart. You can select indicators by clicking at the "Indicators" header and selecting an indicator group from the list of groups below it. This will make the indicators in the selected group appear in the list under "Available indicators" to the left. From that list you can double click on any indicator in order to select it, this will move it to the list under "Selected indicators". Alternatively you can mark one or more indicators and click the single-arrow button. To select all indicators you simply click on the double-arrow button. To deselect indicators you can do correspondingly in the "Selected indicators" list.

To select data elements click on the "Data elements" header. The same principle for selecting and deselecting applies as for indicators.

Selecting reporting rates
=========================
The visualizer can display reporting rates in a chart, by itself or together with indicators and data elements. Reporting rates can be selected by clicking at the "Reporting rates" header. Reporting rates are defined by data sets. It can be selected by double-clicking in the list of available data sets to the left.

Selecting fixed and relative periods
====================================
Click on the "Periods" header. For fixed periods, select a period type from the combo box. You can select any number of fixed periods from any period type. Below the fixed period you will find the relative period checkboxes and you may select as many as you like. The names should be fairly self-descriptive and they are relative to the current date, meaning that if the current month is March and you select "Last month", the month of February will be included in the chart. You are also free to combine fixed periods and relative periods in the same chart. Overlapping periods will be filtered so that they only appear once.

Selecting organisation unit
===========================
You can select which organisation units to include in the chart by clicking the "Organisation units" header. This section features three ways of selecting organisation units. The default mode is called "Organisation units" and lets you select the organisation units you want to appear in the chart from the tree. This mode also features three checkboxes. Checking "User org unit" will disable the organisation unit tree and give you the organisation unit that is related to the current/logged in user instead. This is also useful for administrators as they can create a meaningful "system" favorite with this option checked and all users will find their respective organisation unit when they open it. The the same concept goes for "Org unit children" and "Org unit grand children". The second mode is called "Select levels". Here you can select all organisation units at one or more levels. However, at the same time you also have the option to select parent organisation units in the tree, which makes it easy to select e.g. all facilities inside one or more districts. The same thing goes for the third mode called "Select groups". Here you can select all organisation units inside one or more groups and parent organisation units at the same time.

Selecting organisation unit group sets and data element group sets
==================================================================
All dimension tabs listed below "Organisation units" are organisation unit group sets and data element group sets. You are free to add groups from any of these group sets to your chart. Remember to add the group set in either the series, category or filters combobox.

Selecting chart options
=======================

You can set various chart options by clicking on the "Options" button the chart toolbar.

* Show values: Shows the values above the series in the chart.

* Hide empty category items: Hides category items with no data from the chart.

* Show trend lines: The trend line will visualize how your data evolves over time - e.g. is performance improving or deteriorating. Makes sense when periods are selected as category.

* Target line value/title: Displays a horizontal line at the given domain value. Useful e.g. when you want to compare your performance to the current target.

* Base line value/title: Displays a horizontal line at the given domain value. Useful e.g. when you want to visualize how your performance has evolved since the beginning of a process.

* Range axis max/min: Defines the maximum and minium value which will be visible on the range axis.

* Range axis tick steps: Defines the number of ticks which will be visible on the range axis.

* Range axis decimals: Defines the number of decimals which will be used for range axis values.

* Range axis title: Displays a label next to the range axis (also referred to as the Y axis). Can give context information to the chart, e.g. the unit of measure being used.

* Domain axis title: Displays a label below the domain axis (also referred to as the X axis). Can give context information to the chart, e.g. the type of periods being listed.

* Hide chart legend: Hides the legend and leaves more room for the chart itself.

* Hide chart title: Hides the title of your chart.

* Chart title: Type any title you like and it will appear above the chart.

Displaying a chart
==================

You can display a chart based on your selections simply by clicking the "Update" button on the top centre menu. This requires that you have selected one or more elements from all of the three dimensions - data (indicators, data elements, reporting rates), periods (relative, fixed) and organisation units (units or groups). Note that "Months this year" from the period dimension and the root organisation unit are selected by default.

Notice that you can hide and show individual data series in the chart by clicking directly on the series label in the chart - they appear either at the top or to the right of the chart.

If you want to give the chart more space on your screen you can click on the triple left-arrow button on the top centre menu. This will collapse the left side menu. You can get this menu back by clicking on the same button again.

Downloading chart as image or PDF
=================================
After you have rendered a chart you can download it to your local computer as and image or pdf by clicking on "Download" on the top centre menu. The file will be automatically downloaded to your computer - for instance can you now embed the image file into a text document as part of a report. You can also download the data source behind the chart in json, xml, csv or Microsoft Excel format.

Saving chart as favorite
========================
Once you have rendered a chart you can save it as a favorite to able to access it easily at a later point. Click on the "Favorites" button on the top menu to open up the favorites window. Click "Add new" and in the name field enter the desired name for your chart. The chart will be visible only to yourself. For every favorite in the list you have four options to the right. You can rename the chart (grey button), overwrite the chart (green button), modify the sharing settings of the chart (blue button) or delete the chart (red button).

These favorite charts can later be included on your personal dashboard. After saving you can navigate to the dashboard module, click on the "Insert" link over the chart areas and select your preferred chart.

.. _favorites:
.. figure::  images/favorites.png
   :align:   center
  
Sharing interpretations
=======================
For certain analysis-related resources in iROAD, like pivot tables, charts and maps, one can share a data interpretation. An interpretation is simply a link to the relevant resource together with a text expressing some insight about the data. If you want to share a chart interpretation you need to first save the chart you want to share as a favorite. Then, without making any changes to the chart, click the "Share" button the toolbar. A window will open up and this is where you write your interpretation. When you are done, click share button in the bottom right corner of the window. The window will close automatically and if the interpretation was shared successfully you will find a notification on the bottom toolbar.

Embed charts in any web page
============================
Certain analysis-related resources in iROAD, like pivot tables, charts and maps, can be embeded in any web page by using a plugin. If you have created a chart in the Data Visualizer you will get the plugin configuration for this chart by clicking the "Share" button the toolbar and then "Embed as plugin". You will find more information about the plugins in the web api chapter.


Analysis integration
====================
The analysis apps in iROAD 2 are completely integrated, so you can easily switch between pivot table, chart and map visualization of your data. When you have made a chart you can click e.g. "Map" in the top right corner and then select "Open this table as map".

.. _chart_integration:
.. figure::  images/chart_integration.png
   :align:   center
   
Exiting the data visualizer module
==================================
If you want to exit the module and go back to the iROAD start page you can click on the "Home" button to the right side of the top centre menu.
