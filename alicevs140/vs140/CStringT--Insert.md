---
title: "CStringT::Insert"
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
ms.assetid: a3a32b1a-f223-4467-8886-42fa815898fc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::Insert
Inserts a single character or a substring at the given index within the string.  
  
## Syntax  
  
```  
int Insert(  
   int iIndex,  
   PCXSTR psz  
);  
int Insert(  
   int iIndex,  
   XCHAR ch  
);  
```  
  
#### Parameters  
 `iIndex`  
 The index of the character before which the insertion will take place.  
  
 `psz`  
 A pointer to the substring to be inserted.  
  
 `ch`  
 The character to be inserted.  
  
## Return Value  
 The length of the changed string.  
  
## Remarks  
 The `iIndex` parameter identifies the first character that will be moved to make room for the character or substring. If `nIndex` is zero, the insertion will occur before the entire string. If `nIndex` is higher than the length of the string, the function will concatenate the present string and the new material provided by either `ch` or `psz`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#122](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#122)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)