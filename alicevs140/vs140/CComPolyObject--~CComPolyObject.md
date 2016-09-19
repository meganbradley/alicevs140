---
title: "CComPolyObject::~CComPolyObject"
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
ms.assetid: 6665e890-d698-4d76-b36e-27965ad3b184
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPolyObject::~CComPolyObject
The destructor.  
  
## Syntax  
  
```  
  
~CComPolyObject( );  
  
```  
  
## Remarks  
 Frees all allocated resources, calls [FinalRelease](../vs140/CComPolyObject--FinalRelease.md), and decrements the module lock count.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComPolyObject Class](../vs140/CComPolyObject-Class.md)   
 [CComPolyObject::FinalRelease](../vs140/CComPolyObject--FinalRelease.md)