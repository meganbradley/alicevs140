---
title: "CStringData::IsLocked"
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
ms.assetid: aca3cc00-7411-4955-aa2a-5eeda8ba2aa6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringData::IsLocked
Determines if the character buffer is locked.  
  
## Syntax  
  
```  
  
bool IsLocked( ) const throw( );  
  
```  
  
## Return Value  
 Returns **true** if the buffer is locked; otherwise **false**.  
  
## Remarks  
 Call this function to determine if the character buffer of a string object is currently locked.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStringData Class](../vs140/CStringData-Class.md)