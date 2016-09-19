---
title: "Collecting Thread and Process Concurrency Data"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fa03d381-a9ee-408c-876d-05111e29225b
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collecting Thread and Process Concurrency Data
The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools concurrency profiling method enables you to collect resource contention data that includes information about every synchronization event that causes a function in the profiled application to wait for access to a resource.  
  
 **Requirements**  
  
-   [!INCLUDE[vsUltLong](../vs140/includes/vsUltLong_md.md)], [!INCLUDE[vsPreLong](../vs140/includes/vsPreLong_md.md)], [!INCLUDE[vsPro](../vs140/includes/vsPro_md.md)]  
  
 You can specify the concurrency profiling method by using one of the following procedures:  
  
-   On the first page of the Profiling Wizard, click **Concurrency**  
  
-   On the **General** page of the properties dialog box for the performance session, click **Concurrency**.  
  
-   On the **Performance Explorer** toolbar, in the **Method** list, click **Concurrency**.  
  
## Common Tasks  
 You can specify additional options in the *Performance Session***Property Pages** dialog box of the performance session. To open this dialog box:  
  
-   In **Performance Explorer**, right-click the performance session name, and then click **Properties**.  
  
 The tasks in the following table describe options that you can specify in the *Performance Session***Property Pages** dialog box when you profile by using the concurrency method.  
  
|Task|Related Content|  
|----------|---------------------|  
|On the **General** page, specify naming details for the generated profiling data (.vsp) file.|-   [How to: Set Profiling Data File Options](../vs140/How-to--Set-Performance-Data-File-Name-Options.md)|  
|On the **Launch** page, specify the application to start if you have multiple .exe projects in your code solution.|-   [How to: Specify the Binary to Start](../vs140/How-to--Specify-the-Binary-to-Start.md)|  
|On the **Tier Interaction** page, add ADO.NET call data to the profiling run.|-   [How to: Collect Interaction Data for Multi-Tiered Applications](../vs140/Collecting-tier-interaction-data.md)|  
|On the **Windows Counters** page, specify one or more operating system performance counters to add to the profiling data as marks.|-   [How to: Collect Windows Counter Data](../vs140/How-to--Collect-Windows-Counter-Data.md)|  
|On the **Advanced** page, specify the version of the .NET Framework run-time to profile if your application modules use multiple versions. By default, the first version loaded is profiled.|-   [How to: Specify the .NET Framework Runtime to Profile in Side by Side Scenarios](../vs140/How-to--Specify-the-.NET-Framework-Runtime.md)|