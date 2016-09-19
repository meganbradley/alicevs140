---
title: "CStringT::ReverseFind"
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
ms.assetid: fa953807-03ce-4169-9683-7d922511ae9b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::ReverseFind
Searches this `CStringT` object for the last match of a character.  
  
## Syntax  
  
```  
int ReverseFind(  
   XCHAR ch  
) const throw();  
```  
  
#### Parameters  
 `ch`  
 The character to search for.  
  
## Return Value  
 The zero-based index of the last character in this `CStringT` object that matches the requested character, or –1 if the character is not found.  
  
## Remarks  
 The function is similar to the run-time function `strrchr`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#130](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#130)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)   
 [strrchr, wcsrchr, _mbsrchr, _mbsrchr_l](../vs140/strrchr--wcsrchr--_mbsrchr--_mbsrchr_l.md)