---
title: "CFileTime::SetTime"
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
ms.assetid: 27a91a3b-eab9-4615-895a-f4be5aa3ceaf
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::SetTime
Call this method to set the date and time stored by the `CFileTime` object.  
  
## Syntax  
  
```  
  
      void SetTime(  
   ULONGLONG nTime   
) throw( );  
```  
  
#### Parameters  
 `nTime`  
 The 64-bit value representing the date and time, in either local or Coordinated Universal Time (UTC) format.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)   
 [CFileTime::GetTime](../vs140/CFileTime--GetTime.md)