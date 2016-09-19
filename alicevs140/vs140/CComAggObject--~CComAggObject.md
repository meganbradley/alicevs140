---
title: "CComAggObject::~CComAggObject"
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
ms.assetid: 9321cbf9-28ba-49b2-b4c0-57a5ecea9723
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAggObject::~CComAggObject
The destructor.  
  
## Syntax  
  
```  
  
~CComAggObject( );  
  
```  
  
## Remarks  
 Frees all allocated resources, calls [FinalRelease](../vs140/CComAggObject--FinalRelease.md), and decrements the module lock count.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComAggObject Class](../vs140/CComAggObject-Class.md)