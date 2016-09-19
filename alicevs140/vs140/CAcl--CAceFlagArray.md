---
title: "CAcl::CAceFlagArray"
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
ms.assetid: 6e15409f-e8b7-40a9-95a2-c0d8748a7348
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAcl::CAceFlagArray
An array of BYTEs.  
  
## Syntax  
  
```  
  
typedef CAtlArray<BYTE> CAceFlagArray;  
  
```  
  
## Remarks  
 This typedef specifies the array type used to define the access-control entry (ACE) type-specific control flags. See the [ACE_HEADER](http://msdn.microsoft.com/library/windows/desktop/aa374919) definition for the complete list of possible flags.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAcl Class](../vs140/CAcl-Class.md)   
 [ACE_HEADER](http://msdn.microsoft.com/library/windows/desktop/aa374919)