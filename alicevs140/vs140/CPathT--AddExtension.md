---
title: "CPathT::AddExtension"
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
ms.assetid: 21b0c253-6ea3-4976-b9ea-16ab7b94d37b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::AddExtension
Call this method to add a file extension to a path.  
  
## Syntax  
  
```  
  
      BOOL AddExtension(  
   PCXSTR pszExtension   
);  
```  
  
#### Parameters  
 `pszExtension`  
 The file extension to add.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 For more information, see [PathAddExtension](http://msdn.microsoft.com/library/windows/desktop/bb773563).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)