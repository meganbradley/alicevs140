---
title: "CUrl::GetExtraInfo"
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
ms.assetid: 4d3122b6-d45a-47d4-be64-54d5bfe13b75
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::GetExtraInfo
Call this method to get extra information (such as ?*text* or #*text*) from the URL.  
  
## Syntax  
  
```  
  
inline LPCTSTR GetExtraInfo( ) const throw( );  
  
```  
  
## Return Value  
 Returns a string containing the extra information.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetExtraInfoLength](../vs140/CUrl--GetExtraInfoLength.md)   
 [CUrl::SetExtraInfo](../vs140/CUrl--SetExtraInfo.md)