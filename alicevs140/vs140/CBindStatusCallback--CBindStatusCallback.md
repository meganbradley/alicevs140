---
title: "CBindStatusCallback::CBindStatusCallback"
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
ms.assetid: e64974f7-6a0f-49bd-8dbd-cb22df7f26ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::CBindStatusCallback
The constructor.  
  
## Syntax  
  
```  
  
CBindStatusCallback( );  
```  
  
## Remarks  
 Creates an object to receive notifications concerning the asynchronous data transfer. Typically, one object is created for each bind operation.  
  
 The constructor also initializes [m_pT](../vs140/CBindStatusCallback--m_pT.md) and [m_pFunc](../vs140/CBindStatusCallback--m_pFunc.md) to **NULL**.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md)