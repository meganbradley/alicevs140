---
title: "CUrl::GetExtraInfoLength"
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
ms.assetid: 356deb0b-07df-40ee-8afa-72ba3e30903b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::GetExtraInfoLength
Call this method to get the length of the extra information (such as ?*text* or #*text*) to retrieve from the URL.  
  
## Syntax  
  
```  
  
inline DWORD GetExtraInfoLength( ) const throw( );  
  
```  
  
## Return Value  
 Returns the length of the string containing the extra information.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetExtraInfo](../vs140/CUrl--GetExtraInfo.md)