---
title: "CAtlAutoThreadModuleT::GetDefaultThreads"
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
ms.assetid: 6781f822-47c8-4217-9ba1-52d19e45073f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlAutoThreadModuleT::GetDefaultThreads
This static function dynamically calculates and returns the maximum number of threads for the EXE module, based on the number of processors.  
  
## Syntax  
  
```  
  
static int GetDefaultThreads( );  
  
```  
  
## Return Value  
 The number of threads to be created in the EXE module.  
  
## Remarks  
 Override this method if you want to use a different method for calculating the number of threads. By default, the number of threads is based on the number of processors.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlAutoThreadModuleT Class](../vs140/CAtlAutoThreadModuleT-Class.md)