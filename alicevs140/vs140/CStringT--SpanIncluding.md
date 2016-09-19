---
title: "CStringT::SpanIncluding"
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
ms.assetid: a73660c8-1ec0-4b6d-8571-a032de370cc7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::SpanIncluding
Extracts characters from the string, starting with the first character, that are in the set of characters identified by `pszCharSet`.  
  
## Syntax  
  
```  
CStringT SpanIncluding(  
   PCXSTR pszCharSet  
) const;  
```  
  
#### Parameters  
 `pszCharSet`  
 A string interpreted as a set of characters.  
  
## Return Value  
 A substring that contains characters in the string that are in `pszCharSet`, beginning with the first character in the string and ending when a character is found in the string that is not in `pszCharSet.``SpanIncluding` returns an empty substring if the first character in the string is not in the specified set.  
  
## Remarks  
 If the first character of the string is not in the character set, then `SpanIncluding` returns an empty string. Otherwise, it returns a sequence of consecutive characters that are in the set.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#134](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#134)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)