---
title: "CBindStatusCallback::m_dwAvailableToRead"
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
ms.assetid: e5c672d1-7ed8-42fe-a6ee-e2666431c818
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::m_dwAvailableToRead
Can be used to store the number of bytes available to be read.  
  
## Syntax  
  
```  
  
DWORD m_dwAvailableToRead;  
  
```  
  
## Remarks  
 Initialized to zero in `StartAsyncDownload`.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md)