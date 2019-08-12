---
title: "How Tos: Script Access"
date: "2016-06-27"
---

Accessing the Widgets and Variables of Partial from Parent Page through Scripting

Widgets and Variables inside a partial page can be accessed from the parent page script through the 'Widgets' and 'Variables' property exposed in the scope of the partial container widget. **:** access variables and widgets of a partial page loaded in a page named "Main" use following scripts in Main page controller:

  /\*\* to set the "caption" of a label widget (eg label1) of a partial page loaded as a content of panel widget (eg panel1) \*\*/
  Page.Widgets.panel1.Widgets.label1.caption = "New Caption";

  /\*\* to access partial page's Variable (say staticVariable1) in the parent page 'Main' \*\*/:
  Page.Widgets.panel1.Variables.staticVariable1.dataSet = {"dataValue": "new value"};

Accessing the Widgets and Variables of Parent Page from Partial Page through Scripting

can access the Widgets and Variables of parent page from the partial page script through the 'Widgets' and 'Variables' property exposed in the scope of parent page controller. The parent page scope can be accessed through the $parent property of the partial scope. **:** access variables and widgets of parent page from the partial page named "MyPartial" use following scripts in partial page controller:

  /\*\* to set the "caption" of a label widget (eg label1) of parent page \*\*/
  Partial.App.activePage.Widgets.label1.caption = "New Caption";

  /\*\* to access parent page's Variable (say staticVariable1) in the parent page 'Main' \*\*/:
  Partial.App.activePage.Variables.staticVariable1.dataSet = {"dataValue": "new value"};

Accessing the Widgets and Variables of Partial Page within a Container in a Page

can access the Widgets and Variables of partial page set as content to a tab/panel within a page

\[container\_name\].Variables.\[variable\_name\];
Page.Widgets.\[panel\_name\].Variables.\[variable\_name\];
Page.Widgets.\[tab\_content\_name\].Variables.\[variable\_name\];

In the above scripting format, the partial page variables would be available for the panel and default tab in tabs widget as only the panel and default/first tab will have its widgets and variables ready on parent page load. For tab panes other than default tab, the variables and widgets of the respective partial page content would get loaded only on clicking/opening the other tab panes.Linking Variables through Scripting

: Update of a Service Variable should trigger an update of a Live Variable:

1.update((),
 function successHandler (dataSet) {
	//updating second variable’s dataset if first variable’s updation is success 
        Page.Variables.liveVariable1.update();
        },
 function errorHandler(errMsg) {
			//logging error in console if updation on variable fails
       console.log(errMsg);
        });

NOTE: The above-specified example is for Page. For Partial, you will need to replace the word with a

1.update((),
 function successHandler (dataSet) {
	//updating second variable’s dataset if first variable’s updation is success 
        Partial.Variables.liveVariable1.update();
        },
 function errorHandler(errMsg) {
			//logging error in console if updation on variable fails
       console.log(errMsg);
        });