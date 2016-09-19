---
title: "CPathT::IsUNCServerShare"
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
ms.assetid: 7b258b2e-13d7-4266-a62c-301be3fede9a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::IsUNCServerShare
Call this method to determine whether the path is a valid UNC (universal naming convention) share path, \\\\*server*\\*share*.  
  
## Syntax  
  
```  
  
BOOL IsUNCServerShare( ) const;  
  
```  
  
## Return Value  
 Returns TRUE if the path is in the form \\\\*server*\\*share*, or FALSE otherwise.  
  
## Remarks  
 For more information, see [PathIsUNCServerShare](http://msdn.microsoft.com/library/windows/desktop/bb773723).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)   
 [CPathT::IsUNCServer](../vs140/CPathT--IsUNCServer.md)