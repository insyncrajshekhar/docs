---
title: "Configuring APPSeCONNECT"
toc: true
tag: developers
category: "Configuring APPSeCONNECT"
menus: 
    gettingstarted:
        title: "Configuring APPSeCONNECT"
        weight: 6
        icon: fa fa-wpexplorer
        identifier: configuringaec
---

This section gives the overall idea about choosing application, configuring connection, environment setup and execution of the sync process. Step by Step direction is given below:
Login to APPSeCONNECT - View [Home Page](https://portal.appseconnect.com/Account/Login?ReturnUrl=%2f#!) to get the details.

|Modules|Details|
|---|---|
|[Choosing Applications/ Creating Applications](/configuring%20appseconnect/configurations/#process-of-choosing-app) |User needs to choose the applications as per the requirement of the user. This is the very first step while proceeding with the integration process|
|[Configuring Schema and Entity](/configuring%20appseconnect/configurations/#appseconnect-schemaentity)|Every application has its schema and entity and for integrating with applications|
|[Configuring Attributes](/configuring%20appseconnect/configurations/#appseconnect-attributes)|Every schema has its attributes that are needed to be mapped with the destination application for the sync process|
|[Configuring Connector & Creating Connection](/getting%20started/configurations-for-integration/#configuring-connector-while-creating-connection)|Before proceeding with the integration process, users need to configure the connector for creating the connection. |
|[Choosing Touchpoint/Workflow](/getting%20started/configurations-for-integration/#creating-organisation-touchpoint-workflow)|After the creation of the connection, users need to choose the touchpoint/ Workflow for the object that needs to integrate. For E.g. Business Partner Add, Sales Order Add. etc|
|[Transformation & Mapping](/transformation/overview/)|After choosing touchpoint, user needs to map the attributes with the attributes of the destination application.|
|[Deploying connection/ Workflow](/workflow/deploying-and-executing/)|After the configurations are done, the touchpoint/Workflow needs to be deployed to the environment in which it is to be integrated|
|[Environment Configuration & setup](/getting%20started/configurations-for-integration/#configuring-environment---agent-download--cloud-agent-configuration)|Users can setup the environment for the completion of the integration process|

##  Process of Choosing App 

Choose App option enables the user to select applications from the list of pre-packaged apps on the portal. 
User can also get an option for creating a Custom application or technology app. 

1.	Clicking Choose App button, the user gets the view of the following window.
 ![ChooseApp_Dialogbox](/staticfiles/root/media/ChooseApp_Dialogbox.png)
2. A dialog box appears where you will choose the application and version number from the drop down list. Click **SAVE** to save the app.
![ChooseApp_Dialogbox1](/staticfiles/root/media/ChooseApp_Dialogbox1.png)
3. The list of app you choose gets added and listed in the app section of the organization as shown below:
![AppView](/staticfiles/root/media/AppView.png)
4. Each `OP supported app` has four different functionality attached to it - **Schema, Adapters, Functions & Delete**.
![AppComponents](/staticfiles/root/media/AppComponents.png)
5. For [Cloud Supported Applications](/connectors/OLEDB-Credentials/#how-to-add-credentials-for-cloud-integration) the `Credential button` appears along with the other functionality that are attached.
![Cloud-AppComponents](/staticfiles/root/media/Cloud-AppComponents.png)

[Click](/connectors/Overview-of-Connectors/)to view the configuration details of the Connectors.

Here you can view the details of the respective buttons [Schema](/configuring%20appseconnect/configurations/#appseconnect-schemaentity),[Adapters](/configuring%20appseconnect/configurations/#adapter),[Function](/configuring%20appseconnect/configurations/#functions) & [Delete](/configuring%20appseconnect/configurations/#delete).

## Create Application

APPSeCONNECT provides an option to Create `Custom application` and `Technology application` (as per requirements) for the users.
Any App once added is assigned to a particular category. 

Both the process of application creation is given below.

### (a) Create Custom App

The feature of custom app creation enables you to create a custom app with all the required credentials.
The steps are shown below:

1. Go to My Apps section> Choose App> Create Custom App. The following screen appears  
![CustomAPP-Creation1](/staticfiles/root/media/CustomAPP-Creation1.png)
2. In the Custom App Creation Screen the section are divided into - **App Details, Version Details, Protocol Setup & Adapter**
![CustomAPP-Creation2](/staticfiles/root/media/CustomAPP-Creation2.png)  
3. Enter details like- App Name, Description, Category, Stage, Status, Is Cloud Supported, Choose Picture.
* Stage indicates, in what state the App is, for example, it might be in development stage or design stage.
* Some of the predefined categories are : ERP, ECommerce, CRM, Accounting, etc.
* Stage indicates, in what state the App is, for example, it might be in development stage or design stage.
* The Is Cloud Supported checkbox is to check if the version of the App is cloud supported.
4. Click Continue button, it will direct to the Version detail page. Enter the details of the version of the App. 
   The version screen will allow specifying the version number,version description, version definition, supported version, Adapter template.  
![CustomAPP-Creation3](/staticfiles/root/media/CustomAPP-Creation3.png)
5. Click Continue button, it will direct to the Protocol Setup Page. Enter the mandatory field like Protocol Name, Protocol Method.  
![CustomAPP-Creation4](/staticfiles/root/media/CustomAPP-Creation4.png)

Protocol setup will have two sections: 
 1. Either create new protocol on fly which will require them to create protocol file 
  OR 
2. Select from the generic protocol. The generic protocol will generally have adapter assigned to it, if not the adapter needed to be uploaded to next screen.

You can upload/create a Template File. (If you upload a file then it has to be in XSLT format else an error message will be shown).  
![CustomApp-AddNamespace](/staticfiles/root/media/CustomApp-AddNamespace.png)  
In the Add Namespace portion, you can add new namespace by filling Prefix and URL field.
The namespaces added to the template file will be applied to root node only during XSLT generation.  
Click Continue button, it will direct to the Adapter page.Here you can `Upload Adapter or Select Adapter`.  
![CustomApp-UploadAdapter](/staticfiles/root/media/CustomApp-UploadAdapter.png)
Click Continue button, it will redirect you to the Credential section. After execution of all the steps mentioned above you have created a custom App successfully.
The newly created app, can be viewed in the app listing section. 
* You can also check the Checkbox in case it is a 3rd party adapter.
* If you try to upload Extension, follow the steps in Adapter.  
![CustomApp-Extension](/staticfiles/root/media/CustomApp-Extension.png)  
The Upload adapter will allow either selecting generic adapter or upload adapter file specifically.

**ProTip:** 1. If the generic protocol is selected which already have an adapter specified, this section will show that adapter is already selected and only allow extension upload. 
            2. If the generic protocol does not have adapter uploaded, the upload adapter option will be enabled.
{: .notice--info}

  * Select Adapter provides you the option to select Adapter from the list
  ![CustomApp-SelectAdapter](/staticfiles/root/media/CustomApp-SelectAdapter.png)
  * In case of  Upload Adapter, you must give File Name, File Title, Assembly Version and upload Adapter.
  
**Protip**  App Name will take up to 30 characters and will not allow special character except underscore(_)and dot(.)  
The Adapter needs to be in Zip Format else will show an Error message. Selection of the adapter is restricted to only one  The user can edit & delete the custom app & technology app  
{: .notice--info}

### (b) Technology App Creation
The feature of technology app creation in APPSeCONNECT is to ease the process of adding Specific App as per your business requirement.
Technology App Creation wizard provides a single screen where input details like Application Name, 
Description and the Adapter Technology for adding Specific App (a business requirement) can be provided in one go.

The steps are given below:
1. Go to My Apps section> Choose App> Create Technology App. Click on the drop-down icon and select Create Technology APP.  
![TechnologyApp-Creation](/staticfiles/root/media/TechnologyApp-Creation.png)
2. In the screen, Provide the **APP NAME and DESCRIPTION**, Choose the **Adapter Technology** and click SAVE.  
![TechnologyApp-Creation-Screen2](/staticfiles/root/media/TechnologyApp-Creation-Screen2.png)
3. Now you can view the technology application name, successfully added to your List of APPLICATIONS with a default Image. 
![TechnologyApp-Creation-Screen3](/staticfiles/root/media/TechnologyApp-Creation-Screen3.png)
4. You can edit and add image to your app anytime, by clicking on the VIEW button beside the application name.
5. The Connection can be done with both technology applications or one prepackaged and one technology application as shown below.
 ![TechnologyApp-Creation-Screen4](/staticfiles/root/media/TechnologyApp-Creation-Screen4.png)

View [Technology Apps](/connectors/Overview-of-technology-connectors/) section for more details.

**Protip** Currently we are using only these Technology Adapter - FILE, REST, OLEDB & FTP. 
{: .notice--info}

### APPSeCONNECT Schema/Entity
 
 An entity is defined as an object that has a real-world existence. An entity can be a single thing, person, place, or object. For an e-commerce website, Customer, Order, Invoice etc are entities.

* Data can be stored about such entities.
* Each entity has its own characteristics or attributes. For example, `customer id`, `address`, `phone number` are attributes to the `customer` entity. 
* Each customer record in the database serves as an entity item.
* The definition of an entity is called its schema. In other words, the structure of an entity is called its schema.
* If a customer is an entity then the complete set of the various fields associated with it is called its schema.

Schema Image is given below:

![Schema](/staticfiles/root/media/Schema.png)

### APPSeCONNECT Attributes

In APPSeCONNECT, an attribute is a property or characteristic of a schema. If `customer` is a schema, 
then `customer name, email, address` etc. are defined as attributes.  Before defining a schema you need to have a 
proper understanding of the various data fetched via API so that you can define schema properly and provide the 
required attributes.

![attribute](/staticfiles/root/media/attribute.png)

The attributes can be of various types.

* String -  This type of variable is used when you want to store a string value.
* Bool - This type of variable is used when you want to store a boolean value like true or false.
* Date Time - This type of variable is used when you want to store a date time value.
* Number - This type of variable is used when you want to store a numeric value.
* Double - This type of variable is used when you want to store a floating point or double value.
* ComplexObject - When you store an attribute as a collection of several child attributes it is a ComplexObject. For example, if `address` is an attribute,
  then `Street line 1, Street line 2, City, Pin` would exist as child attributes thus making `address` a complex object.
* ComplexObjectCollections - A ComplexObjectCollection may be defined as a collection of complex objects.

Assume that a customer has two shipping addresses. The first address is based in Delaware and 
the other in California. Each address contains the Street Name, Building name, PIN code etc. 
Thus each address would be stored as a complex object attribute. Let the addresses be stored as 
`address1` and `address2`. Now these addresses would be stored as child attributes to the 
parent attribute `address`. Thus `address becomes a ComplexObjectCollection`.

![complexobject-collection-attribute](/staticfiles/root/media/complexobject-collection-attribute.png)

### Custom Attributes

There might be business requirements to create Custom Fields during the creation of 
mapping where the base mapping does not provide an attribute that you are looking for. 
APPSeCONNECT allows you with a feature where you can add your own 
custom attribute and map that with the data coming from the attribute at the other end.

### Actions

Actions are nothing but defining certain tasks like getting data from an application or sending data to an application based on certain conditions and these conditions are defined through an action filter. 

For example, suppose you want to fetch customer(s) data from an eCommerce site and in APPSeCONNECT you define a Customer entity for that.
Now for getting data we can define an action name called `GET`. When you define an action for an entity you need to provide certain information

* Action Name: Name of the action. In some predefined application many adapter logics are written based on this data.
* Action Description: This is the Description of the action. At the time of touchpoint creation actions are selected based on this description.
* Action Filter & Resync Filter Details

### Adding Schemas and Actions of an Application
The user can view the [schemas and the action](/transformation/working-with-schemas-action-filter/) present or can also add schema and add action for each application. 
This section enables the user to view and add the Schema and its Actions.

**Prerequisites:**
1. The User needs to have a valid AEC account.
2. An application is needed to be select for defining the Schemas and its Actions.

**Process:**
1. Login to the APPSeCONNECT Portal with valid credentials.
2. Move into the APPS Page and [Choose any application](/configuring%20appseconnect/configurations/#process-of-choosing-app). 
3. Click on the + sign after adding the application and click on Schema.(In this case, MS Dynamics NAV has been taken for the instance).
![Select-Schema](/staticfiles/root/media/Select-Schema.png)
4. On the Schema Window, the user can view the schemas present or can also add schemas present for the ADD Schema Option.  
![Add-Schema](/staticfiles/root/media/Add-Schema.png)
5. The Actions inside a schema can be viewed by clicking on the + sign. The ADD ACTION option is provided for Adding Actions inside a Schema.
![Add-Action](/staticfiles/root/media/Add-Action.png)

**Protip:** Default Schemas would only be present for the Pre-packaged APPS.
{: .notice--info}

### Adapter
Adapters helps in integration with other applications easy. Adapter represents an interface between an APP and APPSeCONNECT. An adapter is a component which connects your app with APPSeCONNECT. 
There are few responsibilities of an adapter which are defined as under: 

* Create a credentials view which allows connecting to the respective APP where you want to connect.
* Create Push and Pull method inside the adapter which can send and receive data to and from the application.
* Add additional business behavior with respect to the corresponding app.

The [Adapter](/connectors/Version-Extraction-For-Adapter-Upload/) is loaded dynamically by the [Agent](/deployment/overview/) and calls some specific methods using a fixed contract defined as an interface. 

### Extension
Extensions, on the other hand, are the applications which add an extra feature into the E-commerce/ERP platforms making them capable to work with the APPSeCONNECT agent. When an app supports extension, it enables customization.

### Functions
The APPSeCONNECT expression methods are special transformation block used during `mapping`. The platform provides a bunch of helper functionalities which can be used during mapping/action filters/rules etc. These functions can either be provided through the platform, or you can write one as an independent Software Vendor. The three different types are as follows:
* Generic
* Native
* Cloud App Resource

Here you will get the details of [Appresource Functions](/transformation/using-library-methods/) of APPSeCONNECT
### Delete
This button enables to delete selected app from the list.

**ProTip:** Please choose the category correctly because depending on your choice, you might be allowed to add Connectors. This portal do not support connectors between Apps in the same group (As that won't process any business requirement). For instance, migration jobs from SAP B1 to SAP ECC will not be supported at this time. 
{: .notice--info}


