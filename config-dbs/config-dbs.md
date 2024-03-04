# Configuring MySQL DB System


## Introduction

In this lab, you will learn to manage configurations in MySQL DB System.

_Estimated Time:_ 10 minutes


### Objectives

In this lab, you will be guided through the following tasks:

- Create a MySQL Consiguration 
- Copy a MySQL Configuration, change variables and compare them
- Update the MySQL Configuration of a DB system
- Delete unused MySQL Confiigurations

### Prerequisites

- An Oracle Trial or Paid Cloud Account
- Some Experience with MySQL Shell
- Completed Task 3

## Task 1: Create a MySQL Configuration

1. Click **Navigation Menu**,

    ![OCI Console Home Page](./images/homepage.png " home page")

2. Click  **Databases**, then **Configurations**  
    ![menu databases](./images/menu-databases-configurations.png " ")

    Select the root compartment
    ![Select Root compartment](./images/select-compartment.png " ")

3. Select the Click **Create Configuration**
    ![create configuration](./images/create-configuration-list.png " ")

    Enter name

    ```bash
    <copy>MyConfig</copy>
    ```
    Make sure that the compartment name matches the root compartment. 
    ![create configuration](./images/create-configuration-name.png " ")

    
4. Click the Change Shape button and select the MySQL.HeatWave.VM.Standard shape 
    ![create configuration](./images/create-configuration-shape-change.png " ")
    

5. Scroll down, the Variables Information page is displayed.the User Variables (Read/Write) sectiion add the following variables and values:

    * Set max_connections to 200
    * Set sort\_buffer\_size to 500000
    * Set time\_zone to +01:00

    ![create configuration](./images/create-configuration-add-variables.png " ")

    **Note:** You can click the **+Another Variable** to add more rows for configuring more variables

6. Click Create to create the configuration. The configuration Details page is displayed. 
    ![vcn wizard start create](./images/configuration-details.png " ")

7. Scroll down to see the variables that you have configured
    ![vcn wizard start create](./images/configuration-variables.png " ")



## Task 2: Copy a MySQL Configuration

1. On the MyConfig Details page, click **Copy Configuration** to make copy of the MyConfig configuration. 
    ![menu databases](./images/configuration-copy.png " ")

2. The configuration copy page is displayed

    Enter name:

    ```bash
    <copy>MyConfig2</copy>
    ```

    ![menu databases](./imagescopy-configuration-name.png " ")

3. Scroll Down and click the **Initialization Variiables** tab, and enable the **Ignore case in table and schema names** option

    ![menu databases](./images/copy-configuration-change-initializatio.png " ")

4. Click Create to create the MyConfig2 configuration

5. Go back to the configurations list page
    ![menu databases](./images/list-configuration.png " ")

6. Click the context menu of MyConfig and click Copy Configuration 
    ![menu databases](./images/copy-configuration-from-dropdow.png " ")

    The configuration copy page is displayed
    Enter name:
    ```bash
    <copy>MyConfig3</copy>
    ```
    ![menu databases](./images/copy3-configuration-name.png " ")

7. Scroll down to the User variables (read/write) tab and perform the following changes:
    * Change the value of max_connections to 300
    * Change the value time_zone to +02:00. 
    * Click +Another Variable to add another row.

    ![menu databases](./images/copy-configuration-change-variable.png " ")

    *  Select autocomit in the Variable Name and OFF in the Variable value. 

    ![menu databases](./images/copy-configuration-add-variable.png " ")

8. Click Create to create MyConfig3 



## Task 3: Comparing two MySQL Configuration

1. Go back to the configurations list page 
    ![Select Root compartment](./images/list-configuration3.png " ")
    
3. Select the MyConfig2 and MyConfig 3 confiigurations from the configurations list by selecting the check boxes. Then click the Actions button and select Compare from the drop-down menu
    ![Select Root compartment](./images/compare-configuration.png " ")

4. The Compare configurations dialog box is shown. It shows the differences by default. 

    ![Select Root compartment](./images/compare-configurations-default.png " ")

    If you want to view all informatiion of both configurations, click the Show all configuration Information button. 
    ![Select Root compartment](./images/compare-configurations-show-all.png " ")

    Click Close. 

## Task 4: Update the Configuration of a DB System

1. Click **Navigation Menu**, click  **Databases**, then **DB Systems**  
    ![menu databases](./images/menu-dbsystems.png " ")

3. Click on HEATWAVE-DB to view the deatils.  
    ![menu databases](./images/list-dbsystem.png " ")

4. Click the Edit button to edit the DB System
    ![menu databases](./images/edit-dbsystem.png " ")

4. The edit DB system page is shown. Scroll down to the Configuration section, click the Change Configuration button to choose a different configuration.
    ![menu databases](./images/dbsystem-change-configuration.png " ")

    The browse configuration dialog is displayed. Note that it only lists all configurations that match the shape of the DB System.
    Click the Custom button to hide the default configurations 
    ![menu databases](./images/dbsystem-change-configuration-custom.png " ")

    Select MyConfig2 configuration error messahe is displayed, this is because the initilization variable cannot be changed once the DB System has been deployed. 
    ![menu databases](./images/dbsystem-change-configuration-erro.png " ")
    
5. Select the MyConfig3 configuration and click Select a Configuration. 
    ![menu databases](./images/dbsystem-change-configuration-final.png " ")

6. Click Save Changes in the Edit DB System page. HEATWAVE-DB changes to an updating state, after changing the configuration, the database needs to be restarted for the changes to take effect. 
    ![menu databases](./images/dbsystem-change-configuration-save-changes.png " ")

7. After it has restared, the database will change to ACTIVE state and the configuration shows MyConfig3. 
    ![menu databases](./images/dbsystem-active.png " ")


## Task 5: Delete MySQL Configuration

1. Click **Navigation Menu**, then **Configurations**  
    ![menu databases](./images/menu-databases-configurations.png " ")

    Make sure you are in the root compartment
    ![Select Root compartment](./images/select-compartment.png " ")

3. Select the MyConfig3, MyConfig2 and MyConfig configurations by selecting the respective check boxes, click the actions button and select the Delete from the drop down menu
    ![menu databases](./images/delete-configurations.png " ")

4. Click Delete configurations too confirm
    ![menu databases](./images/delete-configurations-confirm.png " ")

5. An error occurs and the deletion of the MyConfig3 configuration fails. Click Show Details to view the reason. 

    ![menu databases](./images/delete-configurations-error.png " ")
    As shown on the details, the MyConfig3 configuration cannot be deleted because it is currently being used by a DB system.
    Click close on the details page. 

6. On the configuration list page, you will notice that MyConfig2 and MyConfig configurations have been deleted.
    ![menu databases](./images/list-configurations.png " ")


You may now **proceed to the next lab**

## Acknowledgements

- **Author** - Perside Foster, MySQL Principal Solution Engineering
- **Contributors** - Mandy Pang, MySQL Principal Product Manager,  Nick Mader, MySQL Global Channel Enablement & Strategy Manager
- **Last Updated By/Date** - Perside Foster, MySQL Solution Engineering, July 2023