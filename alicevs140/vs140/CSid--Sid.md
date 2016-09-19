---
title: "CSid::Sid"
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
ms.assetid: ff2e9c45-62f5-4db4-aa13-79a1534e2365
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid::Sid
Returns the `SID` (security identifier) structure as a string.  
  
## Syntax  
  
```  
  
LPCTSTR Sid( ) const throw(...);  
  
```  
  
## Return Value  
 Returns the `SID` structure as a string in a format suitable for display, storage, or transmission. Equivalent to [ConvertSidToStringSid](http://msdn.microsoft.com/library/windows/desktop/aa376399), although this function is only available on Windows 2000 or later and so is emulated for earlier operating systems.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSid Class](../vs140/CSid-Class.md)