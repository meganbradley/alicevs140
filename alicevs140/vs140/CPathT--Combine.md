---
title: "CPathT::Combine"
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
ms.assetid: fe398c93-91b0-4e80-84cd-2430391b42f5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::Combine
Call this method to concatenate a string representing a directory name and a string representing a file path name into one path.  
  
## Syntax  
  
```  
  
      void Combine(  
   PCXSTR pszDir,  
   PCXSTR pszFile   
);  
```  
  
#### Parameters  
 `pszDir`  
 The directory path.  
  
 *pszFile*  
 The file path.  
  
## Remarks  
 For more information, see [PathCombine](http://msdn.microsoft.com/library/windows/desktop/bb773571).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)