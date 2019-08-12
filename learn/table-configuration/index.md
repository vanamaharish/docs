---
title: "Data Table Configuration"
date: "2016-10-14"
---

You can access the following features from the **Settings** property of a Data Table.

### & Filter Configuration

and Filter facility is particularly helpful when dealing with huge tables. Instead of restricting the data being displayed, the option can be left to the user to decide which data to be displayed.

WaveMaker this can be achieved via the _mode_ property. The various options available are:

- _filter_ - would give a plain table,
-  - to include a search by field widget at the top of the data table, wherein the user can select the field on which the search can be performed,
- _\-column_ - to include filter conditions for each column based on the column data type. The condition could start with, ends with, is null etc. etc.. This feature can be disabled for a specific column from the column settings.

can add Sorting capability to a Data Table, thus allowing the end-user to sort the rows, based upon the column/fields of their choice. By enabling this property, every column header becomes clickable which toggles the display order. This can be overridden at the column level.

case the underlying Variable has the order by field set, that will be honored with priority given to Data Table sort in case of conflict.

\-user can also be provided with a way to select rows and columns of a table.

- the first row by default
- selection can be either
    - with the display of a radio button or
    - with the display of a checkbox. This option is not available for Data Grid with Form layout
- selection needs to be further configured using the On Column Select and On Column Deselect events.
- Quick Edit and Inline Edit, New row position can be specified to be at the bottom or at the top of the Data Table.

[![](../assets/table-config1.png)](../assets/table-config1.png)

is dividing the set of data rows into discrete pages that will allow users to view data in the form of rows across pages. This should allow for easy navigation across pages for viewing and editing of data. This property depends on the underlying variable configuration. The records to be fetched per request decides the page size of the data table. If the records exceed that limit, then they will be displayed on the next page.

**Type**: To make complete use of pagination, the Data Table provides three unique types of pagination.

- – This option gives a next and previous arrow along with the page numbers at the right bottom of the page.
- \- A bar with the total number of pages and number of items on the current page will be displayed along with arrows for pagination.
- – This option gives the next and previous buttons at the bottom of the page which when clicked goes forward or backward one row.

### Data

user can Export the Data Table to an Excel or CSV format. This option is available only when the Data Source is a Variable based on database CRUD APIs or a Variable based upon a java service or depending on a query. ' **Data Size**' property on data table specifies the number of records to be exported. Based on the profile settings limit, records are fetched. If you specify an export data size value, records are fetched based on this value. By default, the value is set to 100, the maximum export size. To export more than 100 records, the max size in the [](http://[supsystic-show-popup id=109]) needs to be changed from the Project Configurations menu of [Workspace](http://[supsystic-show-popup id=107])

the contents displayed in the Data Table will be exported, as opposed to the contents of the entire underlying database table. For each column selected for display, you can customize the export value using Value Expressions. Value Expression to be set for custom fields.

[![](../assets/table-config2.png)](../assets/table-config2.png)

messages to be displayed at various stages of Data Table rendering can be configured. For example, a message to be displayed when No Data is found or while Data loading etc.. Depending upon they layout type selected the message list will vary.

On Error, Message On Add and Message On Update can be configured for CRUD operations in editable grids.

### Styles

to [styling](/learn/app-development/widgets/datalive/datatable/field-configuration/#styling), styles can be applied to rows in the Data Table. Conditional classes can also be applied based upon the data value within the rows.

[![](../assets/table-config3.png)](../assets/table-config3.png)

< Layouts

Configuration >

[1\. Live & Data Widgets](/learn/app-development/widgets/widget-library/#data-live)

- [1.1 Cards](/learn/app-development/widgets/datalive/cards/)
- [1.2 Data Table](/learn/app-development/widgets/datalive/data-table/)
    - [Data Source](/learn/app-development/widgets/datalive/datatable/data-source/)
        - [Variable Source](/learn/app-development/widgets/datalive/datatable/data-source/#variable-source)
        - [Widget Source](/learn/app-development/widgets/datalive/datatable/data-source/#widget-source)
    - [Layouts](/learn/app-development/widgets/datalive/datatable/layouts/)
        - [Editable with Form as Dialog](/learn/app-development/widgets/datalive/datatable/layouts/#efd)
        - [Editable with Form given below the Table](/learn/app-development/widgets/datalive/datatable/layouts/#efb)
        - [Inline Editable](/learn/app-development/widgets/datalive/datatable/layouts/#edi)
        - [Quick Edit](/learn/app-development/widgets/datalive/datatable/layouts/#edq)
        - [Read-Only with details given below](/learn/app-development/widgets/datalive/datatable/layouts/#rof)
        - [Read-only Simple View](/learn/app-development/widgets/datalive/datatable/layouts/#ros)
    - [Table Configuration](/learn/app-development/widgets/datalive/datatable/table-configuration/)
        - [Search & Filter](#search-n-filter)
        - [Sorting](#sorting)
        - [Selection](#selection)
        - [Pagination](#pagin)
        - [Export Data](#export-data)
        - [Message](#message)
        - [Row Styling](#row-style)
    - [Field Configuration](/learn/app-development/widgets/datalive/datatable/field-configuration/)
        - [Column Grouping](/learn/app-development/widgets/datalive/datatable/field-configuration/#grouping)
        - [View Mode](/learn/app-development/widgets/datalive/datatable/field-configuration/#view-mode)
        - [Edit Mode](/learn/app-development/widgets/datalive/datatable/field-configuration/#edit-mode)
        - [Export Options](/learn/app-development/widgets/datalive/datatable/field-configuration/#export)
        - [Filter Options](/learn/app-development/widgets/datalive/datatable/field-configuration/#filtering)
    - [Actions](/learn/app-development/widgets/datalive/datatable/actions/)
        - [Table Specific Actions](/learn/app-development/widgets/datalive/datatable/actions/#table-actions)
        - [Row Specific Actions](/learn/app-development/widgets/datalive/datatable/actions/#row-actions)
        - [Actions Visibility](/learn/app-development/widgets/datalive/datatable/actions/#actions-visibility)
        - [Actions Layout](/learn/app-development/widgets/datalive/datatable/actions/#actions-layout)
    - [Events & Methods](/learn/app-development/widgets/datalive/datatable/datatable-events-methods/)
        - [Events](/learn/app-development/widgets/datalive/datatable/datatable-events-methods/#events)
        - [Methods](/learn/app-development/widgets/datalive/datatable/datatable-events-methods/#methods)
    - [Cases](/learn/app-development/widgets/datalive/datatable/data-table-use-cases/)
- [1.3 Form](/learn/app-development/widgets/datalive/form/)
- [1.4 List](/learn/app-development/widgets/datalive/list/)
- [1.5 Live Form](/learn/app-development/widgets/datalive/live-form/)
- [1.6 Live Filter](/learn/app-development/widgets/datalive/live-filter/)