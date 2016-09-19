---
title: "CInternetConnection::GetSession"
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
ms.assetid: 582b0bb5-4ed9-401a-976e-f3ded15158b0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetConnection::GetSession
Call this member function to get a pointer to the `CInternetSession` object that's associated with this connection.  
  
## Syntax  
  
```  
  
CInternetSession* GetSession( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CInternetSession](../vs140/CInternetSession-Class.md) object associated with this Internet connection object.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetSession Class](../vs140/CInternetSession-Class.md)   
 [CGopherConnection Class](../vs140/CGopherConnection-Class.md)   
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [CHttpConnection Class](../vs140/CHttpConnection-Class.md)