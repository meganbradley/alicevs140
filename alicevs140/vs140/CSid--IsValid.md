---
title: "CSid::IsValid"
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
ms.assetid: bdb22010-2773-4008-9876-d0ffad366f69
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid::IsValid
Tests the `CSid` object for validity.  
  
## Syntax  
  
```  
  
bool IsValid( ) const throw();  
  
```  
  
## Return Value  
 Returns **true** if the `CSid` object is valid, **false** if not. There is no extended error information for this method; do not call `GetLastError`.  
  
## Remarks  
 The `IsValid` method validates the `CSid` object by verifying that the revision number is within a known range and that the number of subauthorities is less than the maximum.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSid Class](../vs140/CSid-Class.md)