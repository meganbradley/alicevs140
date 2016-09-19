---
title: "CComObjectGlobal::Release"
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
ms.assetid: eaf8c7e6-2fee-447f-adbf-d6cb3fc9c6e2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectGlobal::Release
Decrements the reference count of the object by 1.  
  
## Syntax  
  
```  
  
STDMETHOD_(ULONG, Release)( );  
```  
  
## Return Value  
 In debug builds, **Release** returns a value that may be useful for diagnostics and testing. In non-debug builds, **Release** always returns 0.  
  
## Remarks  
 By default, **Release** calls **_Module::Unlock**, where **_Module** is the global instance of [CComModule](../vs140/CComModule-Class.md) or a class derived from it.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectGlobal Class](../vs140/CComObjectGlobal-Class.md)   
 [CComObjectGlobal::AddRef](../vs140/CComObjectGlobal--AddRef.md)