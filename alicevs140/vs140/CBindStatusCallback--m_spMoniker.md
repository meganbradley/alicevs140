---
title: "CBindStatusCallback::m_spMoniker"
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
ms.assetid: a78da8d0-2a52-4952-8186-c7e4dd6208ad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::m_spMoniker
A pointer to the [IMoniker](http://msdn.microsoft.com/library/windows/desktop/ms679705) interface for the URL to use.  
  
## Syntax  
  
```  
  
CComPtr<IMoniker> m_spMoniker;  
  
```  
  
## Remarks  
 Initialized in `StartAsyncDownload`.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md)   
 [CComPtr Class](../vs140/CComPtr-Class.md)