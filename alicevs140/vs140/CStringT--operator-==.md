---
title: "CStringT::operator =="
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
ms.assetid: 1edc0f09-00e2-4760-8723-cc399112d4b3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::operator ==
Determines whether two strings are logically equal.  
  
## Syntax  
  
```  
friend bool operator==(  
   const CStringT& str1,  
   const CStringT& str2  
) throw();  
friend bool operator==(  
   const CStringT& str1  
   PCXSTR psz2  
) throw();  
friend bool operator==(  
   const CStringT& str1,  
   PCYSTR psz2  
) throw();  
friend bool operator==(  
   const CStringT& str1,  
   XCHAR ch2  
) throw();  
friend bool operator==(  
   PCXSTR psz1  
   const CStringT& str2  
) throw();  
friend bool operator==(  
   PCYSTR psz1  
   const CStringT& str2,  
) throw();  
friend bool operator==(  
   XCHAR ch1  
   const CStringT& str2,  
) throw();  
```  
  
#### Parameters  
 `ch1`  
 An ANSI or Unicode character for comparison.  
  
 `ch2`  
 An ANSI or Unicode character for comparison.  
  
 `str1`  
 A `CStringT` for comparison.  
  
 `str2`  
 A `CStringT` for comparison.  
  
 `psz1`  
 A pointer to a null-terminated string for comparison.  
  
 `psz2`  
 A pointer to a null-terminated string for comparison.  
  
## Remarks  
 Tests whether a string or character on the left side is equal to a string or character on the right side, and returns TRUE or FALSE accordingly.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#142](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#142)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)