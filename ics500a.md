<img class="float-right" src="images/j2c-logo.png">

#  **Lab 500 - Part A: Oracle Integration Cloud (OIC) Development Workshop** 

Fusion HCM with ATOM Feeds Pre-Development Lab

## **Introduction**

- Intro

## **Objectives**

- To configure the Oralce Integration Cloud (OIC) environment in order to complete Lab 500B
- The participant will create the connections needed in the integration
- The participant will create a lookup function
- The participant will create an OIC library connection

## **Software Pre-Requisites**
This lab will provide you with the resources you will need to complete subsequent labs in this workshop

**For this lab you will need access to the following:**

1. Internet Connection
2. Web Browser
3. DateTimeLib4.jar File
4. Oracle Cloud Account with Integration Instance Provisioned

---

## **Recommended Web Browser**
Although most modern browsers are supported. We recommend using *Firefox or Chrome*. As of the last update of this lab, Visual Builder Cloud Service (VBCS) best functions using Chrome.  
>If you are having issues with either browser, please clear your cookies or work in private browsing/incognito mode

---
# **Required Set-Up**

## **500a.1: Importing Add Time Function into OIC Library**

**500a.1.1**: From the OIC Home Page, Select the "Integrations" link to be redirected to the "Integration Designer" Page

![](images/oic-1.png)  

**500a.1.2**: From the "Integration Designer" page, select the "Libraries" link

![](images/integration_designer-library.png)  
   
**500a.1.3**: To add a new library, click the Register button. A window will open where you will: browse and upload the .jar file given to you by your instructor and fill out the required fields then click the Create button
![](images/500a/create_lib.png)  

![](images/500a/register_library.png)  

**500a.1.4**: You will be redirected to the configuration page where you will select the file name under the dropdown of the javascript file highlighted in red below
![](images/500a/configure_library-1.png)  

**500a.1.5**: The page will be populated with details to complete the configuration. Select the checkbox for Orchestration under Classification Type and the other fields should populate automatically

<img src="images/500a/configure_library-2.png" width="300px">   ---> 
<img src="images/500a/configure_library-3.png" width="200px"> 

**500a.1.5**: Save, Close and move on to configuring the Scheduler Lookup

## **500a.2: Configure Scheduler Lookup**
**500a.2.1**: From the OIC Home Page, Select the "Integrations" link to be redirected to the "Integration Designer" Page

![](images/oic-1.png)  

**500a.2.2**: From the "Integration Designer" page, select the "Lookups" link

![](images/integration_designer-lookup.png) 

 **500a.2.3**: To add a new lookup, click the Create button. A window will open where you will: browse and upload the .jar file given to you by your instructor and fill out the required fields then click the Create button 

![](images/500a/create_lookup.png)  

![](images/500a/name_lookup.png)  

**500a.2.4**: In this window, click on the "Domain_Name_1" link then click "Edit Domain Name" and name it with the single letter "A" and click OK then repeat with "Domain_Name_2" but name it the single letter "B"

> <img src="images/500a/configure_lookup-1.png" width="450px">
>

> <img src="images/500a/configure_lookup-2.png" width="220px">     
>

> <img src="images/500a/configure_lookup-3.png" width="325px">  

**500a.2.5**: In the first row listed, add the following values:

- _duration_ under column A and _10_ under column B

Then, click the plus sign <img src="images/500a/add-row.png" width="25px"> twice to add two rows

![](images/500a/configure_lookup-4.png)  

**500a.2.6**: In the next two row listed, add the following values:

- _emailalias_ under column A and 
_first.last@email.com_ under column B

- _pagesize_ under column A and _100_ under column B 

![](images/500a/configure_lookup-5.png) 

**500a.2.7**: Save and Close then move on to creating the connections
 

## **500a.3: Create Connections**

**500a.3.1**:  From the OIC Home Page, Select the "Integrations" link to be redirected to the "Integration Designer" Page

![](images/oic-1.png)  

**500a.3.2**: From the "Integration Designer" page, select the "Connections" link

![](images/integration_designer-connections.png)  

**500a.3.3**: To add a new connection, click the Create button. A window will open where you will see our library of pre-built adapters. Scroll or Search for the Oracle HCM Cloud adapter

![](images/500a/create_connection.png) 

![](images/500a/adapter_menu_hcm.png) 

**500a.3.4**: You will be redirected to a configuration page where you will first be prompted to fill out the required fields. Please use the naming convention depicted and you can leave the default role. Once completed, click the Create button.

![](images/500a/name_connection.png) 

**500a.3.5**: 
- Under the Connection Properties, enter the WSDL url which is typically follows this pattern: https://{***HcmInstanceBaseURL***}/fndAppCoreServices/ServiceCatalogService?WSDL

- Under the Security, enter the username and password of the administrator on the instance 

![](images/500a/hcm_connection.png) 

**500a.3.6**: Once completed, save and test your connection. Once you are prompted with a success message, save once more and close. 

<img src="images/testsaveclose.png" width="200px">  

**500a.3.7**: To create the next connection, click the Create button. A window will open where you will see our library of pre-built adapters. Scroll or Search for the REST adapter

![](images/500a/create_connection.png) 

![](images/500a/adapter_menu_rest.png) 

**500a.3.8**: You will be redirected to a configuration page where you will first be prompted to fill out the required fields. Please use the naming convention depicted and you can leave the default role. Once completed, click the Create button.

![](images/500a/.png) 

**500a.3.9**:
- Under the Connection Properties, enter the connection type as **_BASE_**....
**_TLSVersion_** 1.1 is fine
and **_Connection_** URL should just be the Base URL of the HCM instance

- Under the Security, enter the username and password of the administrator on the instance 

![](images/500a/hcm_rest.png) 

**500a.3.10**: Once completed, save and test your connection. Once you are prompted with a success message, save once more and close. 

<img src="images/testsaveclose.png" width="200px">

**500a.3.11**: To create the next connection, click the Create button. A window will open where you will see our library of pre-built adapters. Scroll or Search for the FTP adapter

![](images/500a/create_connection.png) 

![](images/500a/adapter_menu_ftp.png) 

**500a.3.12**: You will be redirected to a configuration page where you will first be prompted to fill out the required fields. Please use the naming convention depicted and you can leave the default role. Once completed, click the Create button.

![](images/500a/ftp_name.png) 

**500a.3.13**:
- Under the Connection Properties, enter ....

- Under the Security, enter the username and password to access the server otherwise please attach the associated private key

**500a.3.14**: Once completed, save and test your connection. Once you are prompted with a success message, save once more and close. 

<img src="images/testsaveclose.png" width="200px">

# **NEXT STEPS:**
IN THE NEXT LAB (500B) YOU WILL GO ON TO BUILD THE FULL INTEGRATION DEPICTED BELOW:

![](images/500b/image46.png) 

This integration does xyz

# **Additional Resources**
 > [What is an API?](https://www.google.com/search?q=what%27s+an+api&spell=1&sa=X&ved=0ahUKEwj2v7yA7KLgAhXdFzQIHazAADsQBQgpKAA&biw=1440&bih=798&dpr=2)

 > [What is an API? -- Video](https://youtu.be/IAFN2UzN784)

 > [Oracle My Services Log In](https://cloud.oracle.com/en_US/sign-in)

--- 
# **THIS LAB IS NOW COMPLETED**
