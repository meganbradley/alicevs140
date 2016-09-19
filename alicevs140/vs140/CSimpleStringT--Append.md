---
title: "CSimpleStringT::Append"
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
ms.assetid: ee448ce2-f91b-4198-a4af-e26bbc883f8b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::Append
Appends a `CSimpleStringT` object to an existing `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      void Append(  
   const CSimpleStringT& strSrc   
);  
void Append(  
   PCXSTR pszSrc,  
   int nLength  
);  
void Append(  
   PCXSTR pszSrc  
);  
```  
  
#### Parameters  
 `strSrc`  
 The `CSimpleStringT` object to be appended.  
  
 `pszSrc`  
 A pointer to a string containing the characters to be appended.  
  
 `nLength`  
 The number of characters to append.  
  
## Remarks  
 Call this method to append an existing `CSimpleStringT` object to another `CSimpleStringT` object.  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::Append`.  
  
 [!CODE [NVC_ATLMFC_Utilities#75](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#75)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::AppendChar](../vs140/CSimpleStringT--AppendChar.md)