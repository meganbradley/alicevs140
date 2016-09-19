---
title: "CPathT::CompactPathEx"
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
ms.assetid: af7f071a-4b15-4e2c-b64e-8d3f52e2cd1b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::CompactPathEx
Call this method to truncate a file path to fit within a given number of characters by replacing path components with ellipses.  
  
## Syntax  
  
```  
  
      BOOL CompactPathEx(  
   UINT nMaxChars,  
   DWORD dwFlags = 0   
);  
```  
  
#### Parameters  
 `nMaxChars`  
 The maximum number of characters to be contained in the new string, including the terminating NULL character.  
  
 `dwFlags`  
 Reserved.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 For more information, see [PathCompactPathEx](http://msdn.microsoft.com/library/windows/desktop/bb773578).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)   
 [CPathT::CompactPath](../vs140/CPathT--CompactPath.md)