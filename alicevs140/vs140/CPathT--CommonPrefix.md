---
title: "CPathT::CommonPrefix"
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
ms.assetid: 676c32c6-1433-411b-9185-8d353e468ba2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::CommonPrefix
Call this method to determine whether the specified path shares a common prefix with the current path.  
  
## Syntax  
  
```  
  
      CPathT< StringType > CommonPrefix(  
   PCXSTR pszOther   
);  
```  
  
#### Parameters  
 `pszOther`  
 The path to compare to the current one.  
  
## Return Value  
 Returns the common prefix.  
  
## Remarks  
 A prefix is one of these types: "C:\\\\", ".", "..", "..\\\\". For more information, see [PathCommonPrefix](http://msdn.microsoft.com/library/windows/desktop/bb773574).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)