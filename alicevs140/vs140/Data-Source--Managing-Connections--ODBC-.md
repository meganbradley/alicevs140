---
title: "Data Source: Managing Connections (ODBC)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c0adbcdd-c000-40c6-b199-09ffdc7b6ef2
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Source: Managing Connections (ODBC)
This topic applies to the MFC ODBC classes.  
  
 This topic explains:  
  
-   [How to configure a data source](#_core_configuring_a_data_source).  
  
-   [How a multiuser environment affects a data source and its recordsets](#_core_working_in_a_multiuser_environment).  
  
-   [Why you generalize a connection string to a data source](#_core_generalizing_the_connection_string).  
  
-   [How to connect to a data source](#_core_connecting_to_a_specific_data_source).  
  
-   [How to disconnect from a data source](#_core_disconnecting_from_a_data_source).  
  
-   [How to reuse a CDatabase object](#_core_reusing_a_cdatabase_object).  
  
 Connecting to a data source means establishing communications with a DBMS to access the data. When you connect to a data source from an application through an ODBC driver, the driver makes the connection for you, either locally or across a network.  
  
 You can connect to any data source for which you have an ODBC driver. Users of your application must also have the same ODBC driver for their data source. For more information about redistributing ODBC drivers, see [Redistributing ODBC Components to Your Customers](../vs140/Redistributing-ODBC-Components-to-Your-Customers.md).  
  
##  <a name="_core_configuring_a_data_source"></a> Configuring a Data Source  
 ODBC Administrator is used to configure your data sources. You can also use ODBC Administrator after installation to add or remove data sources. When you create applications, you can either direct your users to the ODBC Administrator to let them add data sources or you can build this functionality into your application by making direct ODBC installation calls. For more information, see [ODBC Administrator](../vs140/ODBC-Administrator.md).  
  
 You can use an Excel file as a data source, and you need to configure the file so that it is registered and appears in the **Select Data Source** dialog box.  
  
#### To use an Excel file as a data source  
  
1.  Configure the file with the ODBC Data Source Administrator.  
  
2.  On the **File DSN** tab, click **Add**.  
  
3.  In the **Create New Data Source** dialog box, select an Excel driver, and then click **Next**.  
  
4.  Click **Browse**, and select the name of the file to be used as a date source.  
  
> [!NOTE]
>  You might need to select **All Files** in the drop-down menu to view the .xls files.  
  
1.  Click **Next**, and then click **Finish**.  
  
2.  In the **ODBC Microsoft Excel Setup** dialog box, select the database Version and Workbook.  
  
##  <a name="_core_working_in_a_multiuser_environment"></a> Working in a Multiuser Environment  
 If multiple users are connected to a data source, they can change data while you are manipulating it in your recordsets. Similarly, your changes might affect other users' recordsets. For more information, see [Recordset: How Recordsets Update Records (ODBC)](../vs140/Recordset--How-Recordsets-Update-Records--ODBC-.md) and [Transaction (ODBC)](../vs140/Transaction--ODBC-.md).  
  
##  <a name="_core_generalizing_the_connection_string"></a> Generalizing the Connection String  
 The wizards use a default connection string to establish a connection to a data source. You use this connection to view tables and columns while you are developing your application. However, this default connection string might not be appropriate for your users' connections to the data source through your application. For example, their data source and the path to its location might be different from the one used in developing your application. In that case, you should reimplement the [CRecordset::GetDefaultConnect](../vs140/CRecordset--GetDefaultConnect.md) member function in a more generic fashion and discard the wizard implementation. For example, use one of the following approaches:  
  
-   Register and manage the connection strings using ODBC Administrator.  
  
-   Edit the connection string and remove the data source name. The framework supplies ODBC as the data source; at run time, ODBC displays a dialog box asking for the data source name and any other required connection information.  
  
-   Supply the data source name only. ODBC asks for the user ID and password, if required. For example, before generalizing, the connection string looks like this:  
  
    ```  
    CString CApp1Set::GetDefaultConnect()  
    {  
       return "ODBC;DSN=afx;Trusted_Connection=Yes;";  
    }  
    ```  
  
     This connection string specifies a trusted connection, which uses Windows NT integrated security. You should avoid hard-coding a password or specifying a blank password, because doing so creates a major security weakness. Instead, you can give `GetDefaultConnect` a new connection string so that it queries for a user ID and password.  
  
    ```  
    // User must select data source and supply user ID and password:  
        return "ODBC;";  
    // User ID and password required:  
        return "ODBC;DSN=mydb;";  
    // Password required (myuserid must be replaced with a valid user ID):  
        return "ODBC;DSN=mydb;UID=myuserid;";  
    // Hard-coded user ID and password (SECURITY WEAKNESS--AVOID):  
        return "ODBC;DSN=mydb;UID=sa;PWD=777;";  
    ```  
  
##  <a name="_core_connecting_to_a_specific_data_source"></a> Connecting to a Specific Data Source  
 To connect to a specific data source, your data source must already have been configured with [ODBC Administrator](../vs140/ODBC-Administrator.md).  
  
#### To connect to a specific data source  
  
1.  Construct a `CDatabase` object.  
  
2.  Call its `OpenEx` or **Open** member function.  
  
 For more information about how to specify the data source if it is something other than the one you specified with a wizard, see [CDatabase::OpenEx](../vs140/CDatabase--OpenEx.md) or [CDatabase::Open](../vs140/CDatabase--Open.md) in the *MFC Reference*.  
  
##  <a name="_core_disconnecting_from_a_data_source"></a> Disconnecting from a Data Source  
 You must close any open recordsets before calling the **Close** member function of `CDatabase`. In recordsets associated with the `CDatabase` object you want to close, any pending `AddNew` or **Edit** statements are canceled and all pending transactions are rolled back.  
  
#### To disconnect from a data source  
  
1.  Call the `CDatabase` object's [Close](../vs140/CDatabase--Close.md) member function.  
  
2.  Destroy the object unless you want to reuse it.  
  
##  <a name="_core_reusing_a_cdatabase_object"></a> Reusing a CDatabase Object  
 You can reuse a `CDatabase` object after disconnecting from it, whether you use it to reconnect to the same data source or to connect to a different data source.  
  
#### To reuse a CDatabase object  
  
1.  Close the object's original connection.  
  
2.  Instead of destroying the object, call its `OpenEx` or **Open** member function again.  
  
## See Also  
 [Data Source (ODBC)](../vs140/Data-Source--ODBC-.md)   
 [Data Source: Determining the Schema of the Data Source (ODBC)](../vs140/Data-Source--Determining-the-Schema-of-the-Data-Source--ODBC-.md)   
 [CRecordset Class](../vs140/CRecordset-Class.md)