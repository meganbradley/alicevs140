---
title: "CUrl::SetExtraInfo"
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
ms.assetid: 0d390bbe-55d8-4371-b370-ed66d436092a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::SetExtraInfo
Call this method to set the extra information (such as ?*text* or #*text*) of the URL.  
  
## Syntax  
  
```  
  
      inline BOOL SetExtraInfo(  
   LPCTSTR lpszInfo   
) throw( );  
```  
  
#### Parameters  
 *lpszInfo*  
 The string containing the extra information to include in the URL.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetExtraInfo](../vs140/CUrl--GetExtraInfo.md)