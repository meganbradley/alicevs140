---
title: "CComObject::Release"
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
ms.assetid: a78e13c7-0ecb-42f4-8d6a-59d391039907
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObject::Release
Decrements the reference count on the object.  
  
## Syntax  
  
```  
  
STDMETHOD_(ULONG, Release)( );  
  
```  
  
## Return Value  
 This function returns the new decremented reference count on the object. In debug builds, the return value may be useful for diagnostics or testing. In non-debug builds, **Release** always returns 0.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObject Class](../vs140/CComObject-Class.md)   
 [CComObject::AddRef](../vs140/CComObject--AddRef.md)