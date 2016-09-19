---
title: "CComClassFactorySingleton::m_spObj"
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
ms.assetid: 4af7d8bf-a721-40d0-af42-855897db4ce6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComClassFactorySingleton::m_spObj
The [CComObjectGlobal](../vs140/CComObjectGlobal-Class.md) object constructed by `CComClassFactorySingleton`.  
  
## Syntax  
  
```  
  
CComPtr<IUnknown> m_spObj;  
  
```  
  
## Remarks  
 Each call to the [CreateInstance](../vs140/CComClassFactorySingleton--CreateInstance.md) method simply queries this object for an interface pointer.  
  
 Note that the current form of `m_spObj` presents a breaking change from the way that `CComClassFactorySingleton` worked in previous versions of ATL. In previous versions the `CComClassFactorySingleton` object was created at the same time as the class factory, during server initialization. In Visual C++.NET 2003, the object is created lazily, on the first request. This change could cause errors in programs that rely on early initialization.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComClassFactorySingleton Class](../vs140/CComClassFactorySingleton-Class.md)