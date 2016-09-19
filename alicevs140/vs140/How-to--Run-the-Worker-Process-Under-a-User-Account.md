---
title: "How to: Run the Worker Process Under a User Account"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b58e97b1-e62a-4318-aea4-52276ea20735
caps.latest.revision: 34
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Run the Worker Process Under a User Account
To set up your computer so that you can run the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process (aspnet_wp.exe or w3wp.exe) under a user account, follow these steps.  
  
## Procedure  
  
#### To run aspnet_wp.exe under a user account  
  
1.  Open the machine.config file, located on your computer in the CONFIG folder under the path where you installed the runtime.  
  
2.  Find the <processModel\> section and change the user and password attributes to the name and password of the user account you want aspnet_wp.exe to run under.  
  
3.  Save the machine.config file.  
  
4.  On [!INCLUDE[WinXPSvr](../vs140/includes/winxpsvr_md.md)], IIS 6.0 is installed by default. The corresponding worker process is w3wp.exe.To run in IIS 6.0 mode with aspnet_wp.exe as the worker process, you must follow these steps:  
  
    1.  Click **Start**, click **Administrative Tools** and then choose **Internet Information Services**.  
  
    2.  In the **Internet Information Services** dialog box, right-click the **Web Sites** folder and choose **Properties**.  
  
    3.  In the **Web Sites Properties** dialog box, choose **Service**.  
  
    4.  Select **Run WWW service in IIS6.0 isolation mode**.  
  
    5.  Close the **Properties** dialog box and **Internet Services Manager**.  
  
5.  Open a Windows Command Prompt and reset the server by running:  
  
    ```  
    iisreset  
    ```  
  
     — or —  
  
    ```  
    net stop iisadmin /y  
    net start w3svc  
    ```  
  
6.  Locate the Temporary [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] Files folder, which should be in the same path as the CONFIG folder. Right-click the Temporary [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] Files folder and choose **Properties** on the shortcut menu.  
  
7.  In the **Temporary ASP.NET Files Properties** dialog box, click the **Security** tab.  
  
8.  Click **Advanced**.  
  
9. In the **Advanced Security Settings for Temporary ASP.Net Files** dialog box, click **Add**.  
  
     The **Select User, Computer, or Group dialog box** appears.  
  
10. Type the user name in the **Enter the object name to select** box, and then click **OK**. The user name must follow this format: DomainName\UserName.  
  
11. In the **Permission Entry for Temporary ASP.NET Files** dialog box, give the user **Full Control**, and then click **OK** to close the **Entry for Temporary ASP.NET Files** dialog box.  
  
12. A **Security** dialog box will appear, and asks if you really want to change the permissions on a system folder. Click **Yes**.  
  
13. Click **OK** to close the **Temporary ASP.NET Files Properties** dialog box.  
  
## See Also  
 [System Requirements](../vs140/ASP.NET-Debugging--System-Requirements.md)