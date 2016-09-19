---
title: "CUrl::SetPassword"
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
ms.assetid: 4d06b311-2b00-4a83-8e9a-7ac8c43b5c6b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::SetPassword
Call this method to set the password.  
  
## Syntax  
  
```  
  
      inline BOOL SetPassword(  
   LPCTSTR lpszPass   
) throw( );  
```  
  
#### Parameters  
 *lpszPass*  
 The password.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetPassword](../vs140/CUrl--GetPassword.md)