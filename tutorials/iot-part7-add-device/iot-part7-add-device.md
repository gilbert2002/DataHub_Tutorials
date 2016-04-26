---
title: Internet of Things (IoT) Adding a new device to the IoT Services
description: Part 7 of 8, Add a new device to your IoT Services
tags: [products>sap-hana, topic>big-data, topic>internet-of-things, tutorial>beginner ]

---

## Prerequisites  
 - **Proficiency:** Beginner
 - **Tutorials:** [Internet of Things (IoT) Explore the SAP HCP IoT Services](http://go.sap.com/developer/tutorials/iot-part6-hcp-services.html)


## Next Steps
 - [Internet of Things (IoT) Connecting your Tessel to IoT Services](http://go.sap.com/developer/tutorials/iot-part8-hcp-services-tessel.html)

## Details
### You will learn  
With the MMS service now deployed, and your user assigned the appropriate role it’s time for to add your device(s) so you can communicate with it. To do this you will add your device to the service.

### Time to Complete
**10 Min**.

---


    ![Application URL](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_1.png)

2. Click on the **View registered devices and device types** tile to open the **IoT Services Cockpit**. You will use this page frequently, so it is worth bookmarking it.

    ![View registered devices](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_2.png)


3. The first step will be to add your device. Click on **Device Types**, then the **+** symbol to create a new device. Give it a simple name that makes sense for what you are doing (e.g. `TesselClimate`, and click **Create**.
    ![New Device Type](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_3.png)


    ![Device definition](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_4.png)

5. In the **Fields** section, click the **+ Add Field** button to add in two more fields, then enter the following for name and data types. Click the **Create** button (bottom right corner) when complete. When the message type is created, copy the **ID** string. You will need it later.

    > Note: Be sure to follow the names and capitalization specified here:

    Name            | Type
    --------------- | -------------
    `timestamp`     | `long`
    `Humidity`      | `double`

    ![Message type definition](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_5a.png)

    The message type ID:

    ![ID value](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_5b.png)


    > This is extremely important, once you click **Create** a pop-up will appear that will display the **OAuth access token** for this new device. Copy that and save it somewhere, you will need it soon.  If you lose it, click into the **Authorization** tab and you can generate a new token.

    ![Device](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_6.png)

7. When the OAuth Access Token is displayed, copy the token ID and save it. Click **Close**.

    ![Device ID](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_8.png)


    ![View Messages](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_9a.png)

    ![View stored messages](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_9b.png)


10. On the **HTTP API** page, you will see an HTTP endpoint something like this:



    {"mode":"sync", "messageType":"6c7a02f24cc32ee07174", "messages":[{"Brightness":23, "Humidity":25.7, "Temperature": 76.5, "timestamp":1431450313}]}
    ```




    ![Server Reply](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_12.png)

13. To verify that the posting worked, switch back **IoT Services Cockpit**, click **View messages received, use sample clients, etc.** tile, then click the **Display stored messages** tile. When the page updates you should see something like this:

    ![Viewing stored messages](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_13.png)



    ![Authorization values](https://raw.githubusercontent.com/SAPDocuments/Tutorials/master/tutorials/iot-part7-add-device/p7_15.png)

16. Select then the “RAW” type and copy and paste in the same content you just had (with a few value changes to make it easier to spot this insert. Make sure you change the `messageType` to your ID.
    {"mode":"sync", "messageType":"6c7a02f24cc32ee07174", "messages":[{"Brightness":25, "Humidity":35.7, "Temperature": 86.5, "timestamp":1431450313}]}
    ```

## Next Steps
 - [Internet of Things (IoT) Connecting your Tessel to IoT Services](http://go.sap.com/developer/tutorials/iot-part8-hcp-services-tessel.html)