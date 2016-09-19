---
title: "CSid::operator =="
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
ms.assetid: 9ff12348-8333-40b9-a9dd-afe2fc9a57c8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid::operator ==
Tests two security descriptor objects for equality.  
  
## Syntax  
  
```  
  
      bool operator==(   
   const CSid &lhs,   
   const CSid &rhs   
) throw(   );  
```  
  
#### Parameters  
 `lhs`  
 The `SID` (security identifier) or `CSid` that appears on the left side of the == operator.  
  
 `rhs`  
 The `SID` (security identifier) or `CSid` that appears on the right side of the == operator.  
  
## Return Value  
 **true** if the security descriptors are equal, otherwise **false**.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSid Class](../vs140/CSid-Class.md)