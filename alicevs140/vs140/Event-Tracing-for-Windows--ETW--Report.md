---
title: "Event Tracing for Windows (ETW) Report"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 81e88162-b88a-40b6-8b85-a232c8096a47
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event Tracing for Windows (ETW) Report
The Event Tracing for Windows (ETW) report lists the ETW events that were recorded in a performance session of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools. ETW data is collected in a binary (.etl) file.  
  
> [!NOTE]
>  You cannot display ETW reports in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] interface.  
  
-   For information about how to collect ETW by using the Profiling Tools from [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] interface, see [How to: Collect Event Tracing for Windows (ETW) Data](../vs140/How-to--Collect-Event-Tracing-for-Windows--ETW--Data.md).  
  
-   For information about how to collect ETW data by using the [VSPerfCmd](../vs140/VSPerfCmd.md) command line tools, see [Events](../vs140/Events--VSPerfCmd-.md).  
  
-   You generate the ETW report by using the **VSReport/Summary:ETW** command. For more information, see [VSReport](../vs140/VSPerfReport.md).  
  
|Column|Description|  
|------------|-----------------|  
|**Timestamp**|Identifies when the event occurred.|  
|**Process ID**|Identifies the process that generated the event.|  
|**Thread ID**|Identifies the thread that generated the event.|  
|**Description**|Identifies the event provider.|  
|**Type**|Identifies the event type.|  
|**Properties**|The properties of the event. Each event is a comma-separated, name-value pair that is enclosed in brackets.|