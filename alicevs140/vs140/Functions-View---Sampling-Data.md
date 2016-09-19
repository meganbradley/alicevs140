---
title: "Functions View - Sampling Data"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 029d5ebb-e551-46b0-b64e-2c553d9dbb8e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Functions View - Sampling Data
The Functions report view for the sampling profile method lists the functions that were sampled during the profiling run.  
  
> [!NOTE]
>  Enhanced security features in Windows 8 and Windows Server 2012 required significant changes in the way the Visual Studio profiler collects data on these platforms. Windows Store apps also require new collection techniques. See [Profiling Windows 8 and Windows Server 2012 applications](../vs140/Performance-Tools-on-Windows-8-and-Windows-Server-2012-applications.md).  
  
|Column|Description|  
|------------|-----------------|  
|**Process ID**|The process ID (PID) of the profiling run.|  
|**Process Name**|The name of the process.|  
|**Module Name**|The name of the module that contains the function.|  
|**Module Path**|The path of the module that contains the function.|  
|**Source File**|The source file that contains the definition for this function.|  
|**Function Name**|The fully qualified name of the function.|  
|**Function Line Number**|The line number of the start of this function in the source file.|  
|**Function Address**|The address of the function.|  
|**Inclusive Samples**|The total number of samples that were collected when this function was executing; that is, the number of samples that were collected when this function was on the call stack. The number includes samples that were collected when functions that were called by this function were executing.|  
|**Inclusive Samples %**|The percentage of all samples in the profiling run that were inclusive samples of this function.|  
|**Exclusive Samples**|The total number of samples that were collected when code in the body of this function was executing; that is, when this function was on the top of the call stack. Samples that were collected in functions that were called by this function are not included.|  
|**Exclusive Samples %**|The percentage of all samples in the profiling run that were exclusive samples of this function.|  
  
## See Also  
 [How to: Customize Profiling Tools Report Views](../vs140/How-to--Customize-Report-View-Columns.md)   
 [Functions View - Profiler .NET Memory Instrumentation Data](../vs140/Functions-View---.NET-Memory-Instrumentation-Data.md)   
 [Functions View - Profiler .NET Memory Sampling Data](../vs140/Functions-View---.NET-Memory-Sampling-Data.md)   
 [Functions View - Profiler Instrumentation Data](../vs140/Functions-View---Instrumentation-Data.md)