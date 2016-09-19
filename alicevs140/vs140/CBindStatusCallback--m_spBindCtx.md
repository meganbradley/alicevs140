---
title: "CBindStatusCallback::m_spBindCtx"
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
ms.assetid: befb6b5d-378c-4d0e-91b2-0331ab0c364f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::m_spBindCtx
A pointer to an [IBindCtx](http://msdn.microsoft.com/library/windows/desktop/ms693755) interface that provides access to the bind context (an object that stores information about a particular moniker binding operation).  
  
## Syntax  
  
```  
  
CComPtr<IBindCtx> m_spBindCtx;  
  
```  
  
## Remarks  
 Initialized in `StartAsyncDownload`.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md)   
 [CComPtr Class](../vs140/CComPtr-Class.md)