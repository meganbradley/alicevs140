---
title: "CPathT::GetDriveNumber"
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
ms.assetid: 54e4c793-5216-4943-9569-42d2190f6a56
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::GetDriveNumber
Call this method to search the path for a drive letter within the range of 'A' to 'Z' and return the corresponding drive number.  
  
## Syntax  
  
```  
  
int GetDriveNumber( ) const;  
  
```  
  
## Return Value  
 Returns the drive number as an integer from 0 through 25 (corresponding to 'A' through 'Z') if the path has a drive letter, or -1 otherwise.  
  
## Remarks  
 For more information, see [PathGetDriveNumber](http://msdn.microsoft.com/library/windows/desktop/bb773612).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)