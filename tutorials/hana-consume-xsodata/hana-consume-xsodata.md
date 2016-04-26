---
title: SAP HANA XS Classic, Consume XSODATA in your SAP HANA XSC Application
description: In this tutorial you will incorporate your XSODATA into your SAP HANA XSC application.
tags: [ products>sap-hana, products>sap-hana-studio, products>sap-hana-cloud-platform, topic>sql, topic>big-data, tutorial>beginner]
---

## Prerequisites  
- [Enable XSODATA in your SAP HANA XSC Application](http://go.sap.com/developer/tutorials/hana-xsodata.html)

## Details

### You will learn  
1. How to create a simple xsodata service.

### Time to Complete
Beginners might take **10 minutes** to execute this tutorial.


### Open the Web-based Development Workbench

#### Using the SAP HANA Developer Edition or SAP HANA Cloud Platform
The workbench allows you to develop on HANA without the need to set up a local development environment.

Login to the [HANA Cloud Cockpit](https://account.hanatrial.ondemand.com/cockpit) with your free developer edition account.

![Databases and schemas](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/hana-consume-xsodata/1.png)

Choose Databases and Schemas, and choose then the instance that you created in the previous tutorials. From here you can access the Workbench.

![Individual instance](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/hana-consume-xsodata/2.png)

You are now in the Editor and can immediately start developing in HANA.

#### Using HANA on Amazon AWS or Microsoft Azure

Access the web page of your HANA server using the IP address of your server.  Enter the address ```http://XXX.XXX.XXX.XXX``` to the address bar of your browser. (Replace ```XXX.XXX.XXX.XXX``` with the IP address of your server.)

On the web page, there is a link in the middle column for **Web-Based Development Workbench**.  Click this link to start the workbench.

### Create your main page

Now that you have created your OData service in the previous tutorial it is time to actually incorporate your service into your application directly. For this you will create a new file called `ìndex.html` 

What you will do now is add a basic table control using the SAPUI5 framework.

```
<!DOCTYPE HTML>
```

### Incorporate your xsodata service

Now to add in JavaScript code to to add the UI5 control.

```
    <SCRIPT language="JavaScript">
```

The last bit is to add the call to the service to your code and you will have a complete application, or at least complete in the sense that is shows your data. Add the following bit right after your variable definition `var aData`

```
        $.ajax
```

### Deploy, Run and Test the Application

Now the application is ready to be tested. As you are developing with the SAP HANA Web-based Development Workbench the application is already deployed and activated. So you can immediately continue to test it:

Select the ```index.html``` file to enable the Run on Server in the toolbar. Then click the Run on Server button:

The application will open in your browser and greet you with Hello World:

![Table of data](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/hana-consume-xsodata/3.png)


### Optional: Related Information
[SAP HANA Development Information - Official Documentation](http://help.sap.com/hana_platform#section6)


*This tutorial is part of the SAP HANA and SAP HANA Cloud Platform tutorials set.*