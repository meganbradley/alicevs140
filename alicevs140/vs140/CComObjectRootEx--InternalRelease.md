---
title: "CComObjectRootEx::InternalRelease"
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
ms.assetid: dc3af62d-9eb9-4f15-86a4-aaa79843f050
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::InternalRelease
Decrements the reference count of a nonaggregated object by 1.  
  
## Syntax  
  
```  
  
ULONG InternalRelease( );  
```  
  
## Return Value  
 In both non-debug and debug builds, this function returns a value which may be useful for diagnostics or testing. The exact value returned depends on many factors such as the operating system used, and may, or may not, be the reference count.  
  
## Remarks  
 If the thread model is multithreaded, **InterlockedDecrement** is used to prevent more than one thread from changing the reference count at the same time.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectRootEx::InternalAddRef](../vs140/CComObjectRootEx--InternalAddRef.md)   
 [InterlockedDecrement](http://msdn.microsoft.com/library/windows/desktop/ms683580)