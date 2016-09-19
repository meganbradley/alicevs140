---
title: "CBindStatusCallback::m_pT"
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
ms.assetid: e9b088ff-e052-4fa7-b714-67457263d337
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::m_pT
A pointer to the object requesting the asynchronous data transfer.  
  
## Syntax  
  
```  
  
T  
* m_pT;  
  
```  
  
## Remarks  
 The `CBindStatusCallback` object is templatized on this object's class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md)