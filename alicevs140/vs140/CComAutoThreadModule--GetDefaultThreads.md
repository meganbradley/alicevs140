---
title: "CComAutoThreadModule::GetDefaultThreads"
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
ms.assetid: a79d1e81-8263-41de-84c6-cb558c2d0209
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoThreadModule::GetDefaultThreads
As of ATL 7.0, `CComAutoThreadModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
static int GetDefaultThreads( );  
  
```  
  
## Return Value  
 The number of threads to be created in the EXE module.  
  
## Remarks  
 This static function dynamically calculates the maximum number of threads for the EXE module, based on the number of processors. By default, this return value is passed to the [Init](../vs140/CComAutoThreadModule--Init.md) method to create the threads.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComAutoThreadModule Class](../vs140/CComAutoThreadModule-Class.md)