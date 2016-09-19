---
title: "CStringT::SpanExcluding"
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
ms.assetid: 616ec369-da29-4d0f-9f38-a523418ac2fa
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::SpanExcluding
Extracts characters from the string, starting with the first character, that are not in the set of characters identified by `pszCharSet`.  
  
## Syntax  
  
```  
CStringT SpanExcluding(  
   PCXSTR pszCharSet  
) const;  
```  
  
#### Parameters  
 `pszCharSet`  
 A string interpreted as a set of characters.  
  
## Return Value  
 A substring that contains characters in the string that are not in `pszCharSet`, beginning with the first character in the string and ending with the first character found in the string that is also in `pszCharSet` (that is, starting with the first character in the string and up to but excluding the first character in the string that is found `pszCharSet`). It returns the entire string if no character in `pszCharSet` is found in the string.  
  
## Remarks  
 `SpanExcluding` extracts and returns all characters preceding the first occurrence of a character from `pszCharSet` (in other words, the character from `pszCharSet` and all characters following it in the string, are not returned). If no character from `pszCharSet` is found in the string, then `SpanExcluding` returns the entire string.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#133](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#133)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)