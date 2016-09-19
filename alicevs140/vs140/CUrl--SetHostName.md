---
title: "CUrl::SetHostName"
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
ms.assetid: c60507e2-c3a5-49d6-a4d8-fa9ab7910e00
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::SetHostName
Call this method to set the host name.  
  
## Syntax  
  
```  
  
      inline BOOL SetHostName(  
   LPCTSTR lpszHost   
) throw( );  
```  
  
#### Parameters  
 `lpszHost`  
 The host name.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetHostName](../vs140/CUrl--GetHostName.md)