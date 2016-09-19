---
title: "How to: Write to an Application Event Log (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cadbc8c1-87af-4746-934e-55b79a4f6e2b
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Write to an Application Event Log (Visual Basic)
You can use the `My.Application.Log` and `My.Log` objects to write information about events that occur in your application. This example shows how to configure an event log listener so `My.Application.Log` writes tracing information to the Application event log.  
  
 You cannot write to the Security log. In order to write to the System log, you must be a member of the LocalSystem or Administrator account.  
  
 To view an event log, you can use **Server Explorer** or **Windows Event Viewer**. For more information, see [ETW Events in the .NET Framework](assetId:///d186276f-6afb-4dfd-bf3c-4251edc2c299).  
  
> [!NOTE]
>  Event logs are not supported on Windows 95, Windows 98, or Windows Millennium Edition.  
  
### To add and configure the event log listener  
  
1.  Right-click app.config in **Solution Explorer** and choose **Open**.  
  
     \- or -  
  
     If there is no app.config file,  
  
    1.  On the **Project** menu, choose **Add New Item**.  
  
    2.  From the **Add New Item** dialog box, choose **Application Configuration File**.  
  
    3.  Click **Add**.  
  
2.  Locate the `<listeners>` section in the application configuration file.  
  
     You will find the `<listeners>` section in the `<source>` section with the name attribute "DefaultSource", which is nested under the `<system.diagnostics>` section, which is nested under the top-level `<configuration>` section.  
  
3.  Add this element to that `<listeners>` section:  
  
    ```  
    <add name="EventLog"/>  
    ```  
  
4.  Locate the `<sharedListeners>` section, in the `<system.diagnostics>` section, in the top-level `<configuration>` section.  
  
5.  Add this element to that `<sharedListeners>` section:  
  
    ```  
    <add name="EventLog"  
        type="System.Diagnostics.EventLogTraceListener, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="APPLICATION_NAME"/>  
    ```  
  
     Replace `APPLICATION_NAME` with the name of your application.  
  
    > [!NOTE]
    >  Typically, an application writes only errors to the event log. For information on filtering log output, see [Walkthrough: Filtering My.Application.Log Output](../Topic/Walkthrough:%20Filtering%20My.Application.Log%20Output%20(Visual%20Basic).md).  
  
### To write event information to the event log  
  
-   Use the `My.Application.Log.WriteEntry` or `My.Application.Log.WriteException` method to write information to the event log. For more information, see [How to: Write Log Messages](../Topic/How%20to:%20Write%20Log%20Messages%20\(Visual%20Basic\).md) and [How to: Log Exceptions in Visual Basic](../vs140/How-to--Log-Exceptions-in-Visual-Basic.md).  
  
     After you configure the event log listener for an assembly, it receives all messages that `My.Applcation.Log` writes from that assembly.  
  
## See Also  
 <xref:Microsoft.VisualBasic.Logging.Log?qualifyHint=True>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException?qualifyHint=False>   
 [Working with Application Logs in Visual Basic](../Topic/Working%20with%20Application%20Logs%20in%20Visual%20Basic.md)   
 [How to: Log Exceptions in Visual Basic](../vs140/How-to--Log-Exceptions-in-Visual-Basic.md)   
 [Walkthrough: Determining Where My.Application.Log Writes Information](../Topic/Walkthrough:%20Determining%20Where%20My.Application.Log%20Writes%20Information%20\(Visual%20Basic\).md)