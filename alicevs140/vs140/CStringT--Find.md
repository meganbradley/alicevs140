---
title: "CStringT::Find"
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
ms.assetid: b5746e07-e4c9-4c9f-a7da-b3a4af75f82e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::Find
Searches this string for the first match of a character or substring.  
  
## Syntax  
  
```  
int Find(  
   PCXSTR pszSub,  
   int iStart=0  
) const throw( );  
int Find(  
   XCHAR ch,  
   int iStart=0  
) const throw( );  
```  
  
#### Parameters  
 `pszSub`  
 A substring to search for.  
  
 `iStart`  
 The index of the character in the string to begin the search with, or 0 to start from the beginning.  
  
 `ch`  
 A single character to search for.  
  
## Return Value  
 The zero-based index of the first character in this `CStringT` object that matches the requested substring or characters; -1 if the substring or character is not found.  
  
## Remarks  
 The function is overloaded to accept both single characters (similar to the run-time function `strchr`) and strings (similar to `strstr`).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#114](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#114)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)