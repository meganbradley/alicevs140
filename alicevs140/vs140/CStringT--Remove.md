---
title: "CStringT::Remove"
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
ms.assetid: 6d86d512-ab97-4a31-9953-ef8de5f1cacc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::Remove
Removes all instances of the specified character from the string.  
  
## Syntax  
  
```  
int Remove(  
   XCHAR chRemove  
);  
```  
  
#### Parameters  
 `chRemove`  
 The character to be removed from a string.  
  
## Return Value  
 The count of characters removed from the string. Zero if the string is not changed.  
  
## Remarks  
 Comparisons for the character are case sensitive.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#129](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#129)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)