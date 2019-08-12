---
title: "Configuring Select Widget using Display and Data Fields"
date: "2017-01-10"
---

A Select widget can be used in various ways based on the source of data. Each type of data source needs a different approach. WaveMaker Select widget works in any one of the following ways:

- [static list of values](/learn/how-tos/configuring-select-widget-static-list-values/)
- [variable data](/learn/how-tos/configuring-select-widget-variable/)
- display and data value fields from a Variable
- [database fields](/learn/how-tos/configuring-select-widget-database-fields/)

Usually, when giving options to the user, one would want the option to make sense to the user while using a totally different value internally within the application. For example, the user may select Male/Female but the value stored could be M/F or 0/1. To cater for such needs, WaveMaker Studio offers an Entry type while creating a Model Variable. Using this option, the developer can specify different fields for the variable – one called dataValue and other called name. For example, you want the user to select gender as Male or Female, but want to use M or F internally.

1. and drop a Select and Label widget onto the canvas.
2. [a Model Variable](http://[supsystic-show-popup id=105]), choose Entry Type
3. the Is List and add the list values. you can also use the text editor to enter the values in JSON format: [![](../assets/sel_vals.png)](../assets/sel_vals.png)
4. the dataset of the Model Variable to the select widget
5. the Datafield property to the dataValue and Display Field to the name fields of the static variable. Set the Default Value, note the default value should correspond to the dataValue and not the name field of the static variable. [![](../assets/sel_vals_props.png)](../assets/sel_vals_props.png)
6. selection made by the user is displayed in a Label widget, by binding the select datavalue to it. [![](../assets/sel_list_res.png)](../assets/sel_list_res.png)
7. the app and see the selected item from the Select widget displayed in the label.

[Use Cases](/learn/app-development/widgets/form-widgets/select-use-cases/)

- [1\. How to use list of values for select widget configuration](/learn/how-tos/configuring-select-widget-static-list-values/)
- [2\. How to use variable for select widget configuration](/learn/how-tos/configuring-select-widget-variable/)
- [3\. How to use display and data value fields for select widget configuration](#)
- [4\. How to use database fields for select widget configuration](/learn/how-tos/configuring-select-widget-database-fields/)
- [5\. How to configure cascading select](/learn/how-tos/configuring-cascading-select/)