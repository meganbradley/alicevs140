---
title: "CComObject::~CComObject"
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
ms.assetid: e42872b3-83e1-4e86-a870-72e89a779dad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObject::~CComObject
The destructor.  
  
## Syntax  
  
```  
  
CComObject( );  
  
```  
  
## Remarks  
 Frees all allocated resources, calls [FinalRelease](../vs140/CComObjectRootEx--FinalRelease.md), and decrements the module lock count.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObject Class](../vs140/CComObject-Class.md)