---
title: "CStringT::Delete"
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
ms.assetid: f92059aa-1e23-4c0f-994d-d0d38d2b2b16
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::Delete
Deletes a character or characters from a string starting with the character at the given index.  
  
## Syntax  
  
```  
int Delete(  
   int iIndex,  
   int nCount = 1  
);  
```  
  
#### Parameters  
 `iIndex`  
 The zero-based index of the first character in the `CStringT` object to delete.  
  
 `nCount`  
 The number of characters to be removed.  
  
## Return Value  
 The length of the changed string.  
  
## Remarks  
 If `nCount` is longer than the string, the rest of the string will be removed.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#113](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#113)]  
  
 **Before: Soccer is best, but hockey is quicker!**  
**After: Soccer best, but hockey is quicker!**   
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)