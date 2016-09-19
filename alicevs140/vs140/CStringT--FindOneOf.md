---
title: "CStringT::FindOneOf"
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
ms.assetid: 32a400a7-c740-472d-9ae7-bf8b874e77ac
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::FindOneOf
Searches this string for the first character that matches any character contained in `pszCharSet`.  
  
## Syntax  
  
```  
int FindOneOf(  
   PCXSTR pszCharSet  
) const throw( );  
```  
  
#### Parameters  
 `pszCharSet`  
 String containing characters for matching.  
  
## Return Value  
 The zero-based index of the first character in this string that is also in `pszCharSet`; –1 if there is no match.  
  
## Remarks  
 Finds the first occurrence of any of the characters in `pszCharSet`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#115](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#115)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)