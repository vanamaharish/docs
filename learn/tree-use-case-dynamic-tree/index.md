---
title: "Tree Use Case - Dynamic Tree"
date: "2016-11-30"
---

If you have a requirement, whereby the user decides the structure of the tree. For example, you are building a folder-file structure and the user decides how many folders and files are to be present in a tree. This section deals with such a situation.

1. a Tree widget and 2 buttons (Add File, Add Folder) onto the canvas
2. the Tree widget and specify a _Variable_ as property, "" [![](../assets/tree_dynamic_design.png)](../assets/tree_dynamic_design.png)
3. the Script tab, use the following script for treeData:
    
    // should be an array of objects consisting of label, icon, children keys
        // populate the initial data
    Page.treeData = \[{
            "label": "folder1",
            "icon": "fa fa-folder",
            "children": \[\]
        }, {
            "label": "folder2",
            "icon": "fa fa-folder",
            "children": \[\]
        }\];
    
4. JavaScript for the onSelect event of the tree widget as:
    
     = $item;
    
5. the buttons addfile and add folder, select JavaScript for the onClick events and add the following code:
    
     = function ($event, widget) {
        // add file
        if (Page.activeTreeElement) {
            if (\_.isArray(Page.activeTreeElement.children)) {
                Page.activeTreeElement.children.push({
                    "label": "new file",
                    "icon": "fa fa-file"
                });
    
            }
        }
    };
    
    Page.addfolderClick = function ($event, widget) {
        // add folder
        if (Page.activeTreeElement) {
            if (\_.isArray(Page.activeTreeElement.children)) {
                Page.activeTreeElement.children.push({
                    "label": "new folder",
                    "icon": "fa fa-folder",
                    "children": \[\]
                });
    
            }
        }
    };
    
6. the page and see two folders given by default. Select one node and click Add File to add files, or Add Folder to add folder.

[Widget Cases](/learn/app-development/widgets/basic/tree/)

- [1\. How to build a tree from static variable](/learn/how-tos/tree-use-case-static-variable/)
- [2\. How to build tree from java service](/learn/how-tos/tree-use-case-java-service/)
- [3\. How to build a dynamic tree](/learn/how-tos/tree-use-case-dynamic-tree/)