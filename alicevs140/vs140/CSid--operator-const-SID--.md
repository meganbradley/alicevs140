---
title: "CSid::operator const SID *"
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
ms.assetid: 9992b8c9-2438-4e14-a665-b06050acbc10
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid::operator const SID *
Casts a `CSid` object to a pointer to a `SID` (security identifier) structure.  
  
## Syntax  
  
```  
  
operator const SID *( ) const throw(...);  
  
```  
  
## Remarks  
 Returns the address of the `SID` structure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSid Class](../vs140/CSid-Class.md)   
 [CSid::GetPSID](../vs140/CSid--GetPSID.md)