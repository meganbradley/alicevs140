---
title: "marker_series::write_alert Method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d5465c7-f862-47a7-b249-4116605075a6
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# marker_series::write_alert Method
Writes an alert to the Concurrency Visualizer trace file.  
  
## Syntax  
  
```  
void write_alert(  
   _In_ LPCTSTR _Format,  
   ...  
);  
```  
  
#### Parameters  
 `_Format`  
 A composite format string that contains text intermixed with zero or more format items, which correspond to objects in the argument list.  
  
## Requirements  
 **Header:** cvmarkersobj.h  
  
 **Namespace:** Concurrency::diagnostic  
  
## See Also  
 [marker_series Class](../vs140/marker_series-Class.md)