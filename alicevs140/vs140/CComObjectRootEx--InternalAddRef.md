---
title: "CComObjectRootEx::InternalAddRef"
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
ms.assetid: 4c666eb4-5e44-43bd-ba50-9f7624eb416b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::InternalAddRef
Increments the reference count of a nonaggregated object by 1.  
  
## Syntax  
  
```  
  
ULONG InternalAddRef( );  
```  
  
## Return Value  
 A value that may be useful for diagnostics and testing.  
  
## Remarks  
 If the thread model is multithreaded, **InterlockedIncrement** is used to prevent more than one thread from changing the reference count at the same time.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectRootEx::InternalRelease](../vs140/CComObjectRootEx--InternalRelease.md)   
 [InterlockedIncrement](http://msdn.microsoft.com/library/windows/desktop/ms683614)