---
title: "CPathT::FindExtension"
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
ms.assetid: aead9cc9-6e93-487d-b616-6d99c3cbc677
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::FindExtension
Call this method to find the position of the file extension within the path.  
  
## Syntax  
  
```  
  
int FindExtension( ) const;  
  
```  
  
## Return Value  
 Returns the position of the "." preceding the extension. If no extension is found, returns –1.  
  
## Remarks  
 For more information, see [PathFindExtension](http://msdn.microsoft.com/library/windows/desktop/bb773587).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)   
 [CPathT::GetExtension](../vs140/CPathT--GetExtension.md)