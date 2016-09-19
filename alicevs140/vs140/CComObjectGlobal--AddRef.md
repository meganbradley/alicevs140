---
title: "CComObjectGlobal::AddRef"
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
ms.assetid: aced4063-d2db-4081-8575-467fc25e3e33
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectGlobal::AddRef
Increments the reference count of the object by 1.  
  
## Syntax  
  
```  
  
STDMETHOD_(ULONG, AddRef)( );  
  
```  
  
## Return Value  
 A value that may be useful for diagnostics and testing.  
  
## Remarks  
 By default, `AddRef` calls **_Module::Lock**, where **_Module** is the global instance of [CComModule](../vs140/CComModule-Class.md) or a class derived from it.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectGlobal Class](../vs140/CComObjectGlobal-Class.md)   
 [CComObjectGlobal::Release](../vs140/CComObjectGlobal--Release.md)