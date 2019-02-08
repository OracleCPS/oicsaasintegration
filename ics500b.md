<img class="float-right" src="images/j2c-logo.png">

# **Lab 500 - Part B: Fusion HCM with ATOM Feeds**  

## **Objectives**

- Objective Needed

## **Introduction**

- Before 

## **Pre-Requisites**
 
- Workshop participant or lab instructor should have already completed [Lab 500a](/ics500a.md)

## **Getting Started**

**For this lab you will need access to the following:**

1. [Lab 500a](/ics500a.md) Completed
2. Internet Connection
3. Web Browser
4. Oracle Cloud Account with Integration Instance Provisioned
5. [getEmployeeResponse.json](/images/500b/other_files/getEmployeeResponse.json)
6. [newEmployeeFile.csv](/images/500b/other_files/newEmployeeFile.csv)

## **500b.1: Log in to the Oracle Integration Cloud Home Page and Nagivate to the Integration Designer Page**
**500b.1.1**: Navigate to the Home Page by using the OIC URL provided to you by your instructor. The URL should have the following pattern: 
https://{**InstanceName**}-{**CloudAccountName**}.integration.ocp.oraclecloud.com/ic/home/

**500b.1.2**: Log in using the IDCS re-route page

![](images/300/image002.png)  

**500b.1.3**: From the home page, select *Integrations* and you should be auto redirected to the Integration Designer Page where you will see a list of the all the integrations available on the environment.

![](images/oic-1.png)

## **500b.2: Create a Scheduled Orchestration**
**500b.2.1**: From the Integrations Designer Page, Select Create and Choose the Integration style _App Driven Orchestration_
![](images/integration_style.png)  

**500b.2.2**: Give the integration a name
![](images/integration_name.png) ***!!!!! ***

**500b.2.2**: Click on the schedule icon and select the pencil to edit the details

<img src="images/500b/image000.png" width="100px">
---> 
<img src="images/500b/image001.png" width="110px">  

**500b.2.2**: 
- Name the Parameter: _ATOMLastRunDateTime_
- Enter the description as: _Last successful processed ATOM pull_
- Enter the value as: 2018-01-01T00:00:00.000Z

Once completed, close to be brought back to the main integration 

![](images/500b/image002.png) 

**500b.2.3**:  

<img src="images/500b/image003.png" width="500px"> 

<img src="images/500b/image004.png" width="500px"> 

**500b.2.4**: 

<img src="images/500b/image005.png" width="100px">

![](images/500b/image006.png)

**500b.2.5**: Select the + Function button and select the addTime function listed in the menu. You will be redirected to a page with two parameters. On the first parameter labeled _ts_, click on the pencil then paste in the following to the expression builder: 
> **_concat(substring-before(/nssrcmpr:schedule/nssrcmpr:startTime,"."),".000Z")_**

Validate, Save, and Close.

**500b.2.6**: Click the pencil icon for the second parameter, _z_ to be redirected to the expression builder. In the Source panel, select and drag the **lookupValue** menu item from the Components>Functions>Integration Cloud menu into the expression builder. 

As a result, the Lookup Wizard will open.

![](images/500b/image007.png)  

The value for the parameter ‘srcValue is not filled….

/nssrcmpr: schedule

![](images/500b/image008.png)



![](images/500b/image009.png)  
![](images/500b/image010.png)  
![](images/500b/image011.png) 



![](images/500b/image012.png)  
![](images/500b/image013.png)  
![](images/500b/image014.png)  
![](images/500b/image015.png)  
![](images/500b/image016.png)  
![](images/500b/image017.png)  
![](images/500b/image018.png)  
![](images/500b/image019.png)  
![](images/500b/image020.png)  
![](images/500b/image021.png)  
![](images/500b/image022.png)  
![](images/500b/image023.png)  
![](images/500b/image024.png)  
![](images/500b/image025.png)  
![](images/500b/image026.png)  
![](images/500b/image027.png)  
![](images/500b/image028.png)  
![](images/500b/image029.png)  
![](images/500b/image030.png)  
![](images/500b/image031.png)  
![](images/500b/image032.png)  
![](images/500b/image033.png)  
![](images/500b/image034.png)  
![](images/500b/image035.png)  
![](images/500b/image036.png)  
![](images/500b/image037.png)  
![](images/500b/image038.png)  
![](images/500b/image039.png)  
![](images/500b/image040.png)  
![](images/500b/image041.png)  
![](images/500b/image042.png)  
![](images/500b/image043.png)  
![](images/500b/image044.png)  
![](images/500b/image045.png)  
![](images/500b/image046.png)  
![](images/500b/image047.png)  
![](images/500b/image048.png)  
![](images/500b/image049.png)  
![](images/500b/image050.png)  
![](images/500b/image051.png)  
![](images/500b/image052.png)  
  



--- 

# **THIS LAB IS NOW COMPLETED. PLEASE SEE YOUR INSTRUCTOR FOR FURTHER INSTRUCTIONS**
> In the next lab, we are going to use AIC Fusion ERP Adapter to process a Fusion ERP FBDI file and load the contents into Fusion ERP.

In this Lab we are going to create an integration flow that retrieves ATOM Feeds from Fusion HCM for processing, for example, New Hire ATOM Feeds.

```
You have now completed Lab 500 of the AIC SaaS Developer Workshop. 

- This Lab is now completed.


