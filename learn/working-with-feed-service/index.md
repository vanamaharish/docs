---
title: "Working with Feed service"
date: "2016-11-22"
---

web feed is a document (often XML-based) whose discrete content items include web links to the source of the content. News websites and blogs are common sources for web feeds, but feeds are also used to deliver structured information ranging from weather data to top-ten lists of hit tunes to search results. The two main web feed formats are RSS and Atom.

1. can **Feed Services** into your WaveMaker apps using the Import -> Web Services option.
2. the Feed service create a **Feed Service**
3. a generic Feed service is imported a **Variable** has to be created using the getFeed operation to set the FeedUrl.
4. Service Variable can then be bound to appropriate depending upon the response format of the service.

# Generic Feed Service

You can import a feed service into your WaveMaker application by following these steps:

1. Main Menu, click Import Web Services [![Web_Service1](../assets/Web_Service1.png)](../assets/Web_Service1.png)
2. the **Service** dialog, click the icon.
3. [![240_FEED](../assets/240_FEED.png)](../assets/240_FEED.png)
4. generic Feed Service is imported to your application and is displayed in the  section of the  **and  Services Panel** on the left under  _Service_ section. [![240_FEEDService](../assets/240_FEEDService.png)](../assets/240_FEEDService.png)

# Variable for Generic Feed Service

To use the Service data within the app, you need a Service Variable.

1. Main Menu, click  and choose [![Var_create](../assets/Var_create.png)](../assets/Var_create.png)
2. the  dialog, select _Variable_ and ; then select as and as the [![web_feed_var](../assets/web_feed_var.png)](../assets/web_feed_var.png)
3. the  tab and set the  URL for your service. Configure other properties of the variable, if required. In this example, we are using the CNN Feed Service: ://rss.cnn.com/rss/edition.rss [![web_feed_data](../assets/web_feed_data.png)](../assets/web_feed_data.png)

# Binding to Display the Feed Response

1. and Drop a List onto the project canvas.
2. the Existing Variable option to select the Service Variable created in the previous step, and select the  node. [![web_feed_list](../assets/web_feed_list.png)](../assets/web_feed_list.png)
3. a Template and Pagination appropriately. We have selected Media List and Basic Pagination style.
4. the fields appropriately. We have bound Name to the author, Time to updatedDate, and Description to description. From the canvas delete unwanted widgets, Picture in this case.
5. the app and see the content displayed. (Ensure that the Request Data on Page Load property is checked for the Service Variable) [![web_feed_listrun](../assets/web_feed_listrun.png)](../assets/web_feed_listrun.png)

4\. Creating Backend Services

- 4.1 Overview
    - [Accessing Data](/learn/app-development/services/creating-backend-services/#accessing-data)
        - [Life-cycle of data](/learn/app-development/services/creating-backend-services/#life-cycle)
    - [Manipulating Data](/learn/app-development/services/creating-backend-services/#manipulating-data)
        - [Life-cycle of Events](/learn/app-development/services/creating-backend-services/#life-cycle-events)
    - [REST APIs](/learn/app-development/services/creating-backend-services/#rest-apis)
- [4.2 Web Services](/learn/app-development/services/web-services/web-services/)
    - [Overview](/learn/app-development/services/web-services/web-services/#overview)
    - [Service Variables](/learn/app-development/services/web-services/web-services/#service-variable)
    - iii. Working with SOAP Services
        - [Overview](/learn/app-development/services/web-services/working-with-soap-services/)
        - [SOAP Service Setup](/learn/app-development/services/web-services/working-with-soap-services/#SOAP-service-setup)
        - [SOAP Service Settings](/learn/app-development/services/web-services/working-with-soap-services/#SOAP-service-settings)
        - [Generated REST APIs](/learn/app-development/services/web-services/working-with-soap-services/#generated-rest-apis)
        - [SOAP Service Usage](/learn/app-development/services/web-services/working-with-soap-services/#SOAP-service-usage)
    - iv. Working with REST Services
        - [ Overview](/learn/app-development/services/web-services/rest-services/)
        - [ Test REST Service](/learn/app-development/services/web-services/rest-services/#test-API)
        - [ Configure REST Service](/learn/app-development/services/web-services/rest-services/#configure-REST-service)
        - [REST Service Usage](/learn/app-development/services/web-services/rest-services/#REST-service-usage)
    - [Working with Feed Service](#)
        - [ Overview](#)
        - [ Importing Feed Service](#importing-generic-feed-service)
        - [Service Variable](#service-variable)
        - [ Widget Binding](#widget-binding)
    - vi. Working with Web Sockets
        - [Overview](/learn/app-development/services/web-services/working-with-websockets/)
        - [Service Integration](/learn/app-development/services/web-services/working-with-websockets/#import)
        - [Service Consumption](/learn/app-development/services/web-services/working-with-websockets/#variable)
        - [Use Cases](/learn/app-development/services/web-services/working-with-websockets/#use-cases)
- 4.3 Database Services
    - i. Working with Databases
        - [Overview](/learn/app-development/services/database-services/#working-with-db)
        - [Database Service Architecture](/learn/app-development/services/database-services/#database-architecture)
        - [Supported Databases](/learn/app-development/services/database-services/#supported-databases)
        - [Integrating Database](/learn/app-development/services/database-services/#integrating-database)
        - [Database Actions](/learn/app-development/services/database-services/#database-actions)
    - ii. Data Modelling
        - [Overview](/learn/app-development/services/database-services/data-modelling/)
        - [Configuration Settings](/learn/services/db-services/data-modelling/#configuration-settings)
        - [Database Designer](/learn/services/db-services/data-modelling/#database-designer)
            - [Schema Import Modes](/learn/app-development/services/database-services/database-schema-import-modes/)
        - ○ Working with Database Schema
            - [Overview](/learn/app-development/services/database-services/working-database-schema/)
            - [Adding Tables and Columns](/learn/app-development/services/database-services/working-database-schema/#add-tables-columns)
            - [Working with Relationships](/learn/app-development/services/database-services/working-database-schema/#database-relationships)
            - [Identity Generators for Primary Key Column](/learn/app-development/services/database-services/working-database-schema/#identity-generators)
            - [Column Metadata Configuration](/learn/app-development/services/database-services/working-database-schema/#column-metadata-configuration)
            - [Virtual Primary Keys and Relations](/learn/app-development/services/database-services/working-database-schema/#virtual-primary-keys)
    - ii. Databases Access
        - [Overview](/learn/app-development/services/database-access/)
        - ○ Working with Queries
            - [Overview](/learn/app-development/services/database-services/working-with-queries/)
            - [Query Editor](/learn/app-development/services/database-services/working-with-queries/#query-editor)
            - [Types of Queries](/learn/app-development/services/database-services/working-with-queries/#query-types)
            - [Query Creation](/learn/app-development/services/database-services/working-with-queries/#query-creation)
            - [Query Usage](/learn/app-development/services/database-services/working-with-queries/#query-usage)
            - [Parameterised Query Creation](/learn/app-development/services/database-services/working-with-queries/#query-creation-parameterised)
            - [Query Operation Type](/learn/app-development/services/database-services/working-with-queries/#query-op-types)
            - [Query Architecture](/learn/app-development/services/database-services/working-with-queries/#query-architecture)
        - ○ Working with Stored Procedures
            - [Overview](/learn/app-development/services/db-services/working-stored-procedures/)
            - [Procedure Creation](/learn/app-development/services/db-services/working-stored-procedures/#procedure-creation)
            - [Procedure Parameters](/learn/app-development/services/db-services/working-stored-procedures/#proc-params)
            - [Procedure Invocation](/learn/app-development/services/db-services/working-stored-procedures/#procedure-invocation)
            - [Procedure Architecture](/learn/app-development/services/db-services/working-stored-procedures/#procedure-architecture)
        - [Versioning of Queries and Procedures](/learn/app-development/services/database-services/versioning-queries-procedures/)
        - [ Blob Support for Queries and Procedures](/learn/app-development/services/database-services/blob-support-queries-procedures/)
        - [Invoking Queries & Procedures from Java Service](/learn/app-development/services/database-services/invoking-queriesprocedures-java-services/)
        - [ Database Views](/learn/app-development/services/db-services/database-views/)
        - ○ Database Tools
            - [Overview](/learn/app-development/services/database-tools/)
            - [DB Shell](/learn/app-development/services/database-tools/#db-shell)
            - [DB Scripts](/learn/app-development/services/database-tools/#db-scripts)
                - [Import DB](/learn/app-development/services/database-tools/#import-db)
                - [Export DB](/learn/app-development/services/database-tools/#export-db)
    - iv. ORM Artifacts
        - [Database Integration Process](/learn/app-development/services/db-services/orm-artifacts/#database-integration-process)
        - [Layered Architecture](/learn/app-development/services/db-services/orm-artifacts/#layered-architecture)
        - [Generated Files](/learn/app-development/services/db-services/orm-artifacts/#generated-files)
        - [Generated APIs](/learn/app-development/services/db-services/orm-artifacts/#generated-apis)
            - [CRUD APIs](/learn/app-development/services/db-services/orm-artifacts/#crud-apis)
            - [Query APIs](/learn/app-development/services/db-services/orm-artifacts/#query-apis)
            - [Custom Query Syntax](/learn/app-development/services/db-services/orm-artifacts/#custom-query-syntax)
- 4.4 Java Services
    - [ Overview](/learn/app-development/services/java-services/java-service/#overview)
    - [Java Services Framework](/learn/app-development/services/java-services/java-service/#java-services-framework)
    - iii. Integration Services
        - [Current Loggedin User](/learn/app-development/services/java-services/java-integration-services/#loggedin-user)
        - [External Java Libraries](/learn/app-development/services/java-services/java-integration-services/#external-java-libraries)
        - [Database Entities](/learn/app-development/services/java-services/java-integration-services/#db-services)
        - [Named Queries](/learn/app-development/services/java-services/java-integration-services/#query-service)
        - [Imported Web Services](/learn/app-development/services/java-services/java-integration-services/#web-services)
    - [Service Variables](/learn/app-development/services/java-services/service-variables/)
    - [ Generated REST APIs](/learn/app-development/services/java-services/generated-rest-apis-api-designer/)
- 4.5 API Designer
    - [Overview](/learn/app-development/services/api-designer/api/)
    - [Database Services APIs](/learn/app-development/services/api-designer/database-service-apis/)
    - [Web Services APIs](/learn/app-development/services/api-designer/web-service-apis/)
    - [Java Services APIs](/learn/app-development/services/api-designer/java-service-apis/)
    - [Security Services APIs](/learn/app-development/services/api-designer/security-service-apis/)
- 4.6 3rd Party Libraries
    - [Overview](/learn/app-development/services/3rd-party-libraries/)
    - [Including resource files](/learn/app-development/services/3rd-party-libraries/#resource-files)
    - [Using third-party JavaScript file](/learn/app-development/services/3rd-party-libraries/using-3rd-party-javascript-files/)
    - [Using third-party jar file](/learn/app-development/services/3rd-party-libraries/using-3rd-party-jar-files/)