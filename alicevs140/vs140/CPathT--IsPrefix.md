---
title: "CPathT::IsPrefix"
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
ms.assetid: 4cd50647-1327-43e6-949d-ce86def48a4b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::IsPrefix
Call this method to determine whether a path contains a valid prefix of the type passed by `pszPrefix`.  
  
## Syntax  
  
```  
  
      BOOL IsPrefix(  
   PCXSTR pszPrefix   
) const;  
```  
  
#### Parameters  
 `pszPrefix`  
 The prefix for which to search. A prefix is one of these types: "C:\\\\", ".", "..", "..\\\\".  
  
## Return Value  
 Returns TRUE if the path contains the prefix, or FALSE otherwise.  
  
## Remarks  
 For more information, see [PathIsPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773650).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)