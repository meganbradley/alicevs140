---
title: "CAccessToken::GetSource"
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
ms.assetid: 85ff88bc-a253-4b8b-a6a6-55d8cbb4bd2d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetSource
Call this method to get the source of the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool GetSource(  
   TOKEN_SOURCE* pSource  
) const throw(...);  
```  
  
#### Parameters  
 *pSource*  
 Pointer to a [TOKEN_SOURCE](http://msdn.microsoft.com/library/windows/desktop/aa379631) structure.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)