---
title: "CPathT::IsUNCServer"
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
ms.assetid: 23a98449-e28a-4ece-9388-4eb3c5e19dc1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::IsUNCServer
Call this method to determine whether the path is a valid UNC (universal naming convention) path for a server only.  
  
## Syntax  
  
```  
  
BOOL IsUNCServer( ) const;  
  
```  
  
## Return Value  
 Returns TRUE if the string is a valid UNC path for a server only (no share name), or FALSE otherwise.  
  
## Remarks  
 For more information, see [PathIsUNCServer](http://msdn.microsoft.com/library/windows/desktop/bb773722).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)   
 [CPathT::IsUNCServerShare](../vs140/CPathT--IsUNCServerShare.md)