---
title: "CAtlServiceModuleT::LogEvent"
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
ms.topic: reference
ms.assetid: 32f1dda0-ee5b-471e-bbf6-657c64b5eb88
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::LogEvent
Writes to the event log.  
  
## Syntax  
  
```  
  
      void __cdecl LogEvent(  
   LPCTSTR pszFormat,  
   ...   
) throw( );  
```  
  
#### Parameters  
 `pszFormat`  
 The string to write to the event log.  
  
 ...  
 Optional extra strings to be written to the event log.  
  
## Remarks  
 This method writes details out to an event log, using the function [ReportEvent](http://msdn.microsoft.com/library/windows/desktop/aa363679). If no service is running, the string is sent to the console.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)