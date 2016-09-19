---
title: "CFileTime::CFileTime"
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
ms.assetid: 007cd898-d617-4ecc-9857-92900a677148
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::CFileTime
The constructor.  
  
## Syntax  
  
```  
  
      CFileTime( ) throw( );   
CFileTime(  
   const FILETIME& ft   
) throw( );  
CFileTime(  
   ULONGLONG nTime   
) throw( );  
```  
  
#### Parameters  
 `ft`  
 A [FILETIME](http://msdn.microsoft.com/library/windows/desktop/ms724284) structure.  
  
 `nTime`  
 The date and time expressed as a 64-bit value.  
  
## Remarks  
 The `CFileTime` object can be created using an existing date and time from a `FILETIME` structure, or expressed as a 64-bit value (in local or Coordinated Universal Time (UTC) time formats). The default constructor sets the time to 0.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)