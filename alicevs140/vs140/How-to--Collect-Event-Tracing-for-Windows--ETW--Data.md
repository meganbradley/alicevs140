---
title: "How to: Collect Event Tracing for Windows (ETW) Data"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aa2261fe-d5f5-49fc-a171-d18842e1dc7d
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Collect Event Tracing for Windows (ETW) Data
Event Tracing for Windows (ETW) is an efficient kernel-level tracing facility that enables profiler log kernel or application-defined events. The data that is collected from the event provider can be viewed only by using the /**Summary:ETW** option of the [VSPerfReport](../vs140/VSPerfReport.md) command-line tool. You can use this report to determine where performance issues occur in the application.  
  
 **Requirements**  
  
-   [!INCLUDE[vsUltLong](../vs140/includes/vsUltLong_md.md)], [!INCLUDE[vsPreLong](../vs140/includes/vsPreLong_md.md)], [!INCLUDE[vsPro](../vs140/includes/vsPro_md.md)]  
  
> [!NOTE]
>  Enhanced security features in Windows 8 and Windows Server 2012 required significant changes in the way the Visual Studio profiler collects data on these platforms. Windows Store apps also require new collection techniques. See [Profiling Windows 8 and Windows Server 2012 applications](../vs140/Performance-Tools-on-Windows-8-and-Windows-Server-2012-applications.md).  
  
### To enable event trace providers  
  
1.  In **Performance Explorer**, right-click the performance session, and then click **Properties**.  
  
2.  In the **Property Pages**, click the **Windows Events** properties.  
  
3.  In the **Select event trace provider to collect data from** list, select the event providers that you want to use to profile your application.  
  
## See Also  
 [Configuring Performance Sessions](../vs140/Configuring-Performance-Sessions.md)