---
title: "CPathT::IsDirectory"
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
ms.assetid: d695b757-7657-4436-9e3b-cde139272a9f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::IsDirectory
Call this method to check whether the path is a valid directory.  
  
## Syntax  
  
```  
  
BOOL IsDirectory() const;  
  
```  
  
## Return Value  
 Returns a non-zero value (16) if the path is a directory, `FALSE` otherwise.  
  
## Remarks  
 For more information, see [PathIsDirectory](http://msdn.microsoft.com/library/windows/desktop/bb773621).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)