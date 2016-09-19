---
title: "CUrl::SetUserName"
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
ms.assetid: 5c21a4a3-864d-4d5d-bece-6bc548736e3a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::SetUserName
Call this method to set the user name.  
  
## Syntax  
  
```  
  
      inline BOOL SetUserName(  
   LPCTSTR lpszUser   
) throw( );  
```  
  
#### Parameters  
 *lpszUser*  
 The user name.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetUserName](../vs140/CUrl--GetUserName.md)