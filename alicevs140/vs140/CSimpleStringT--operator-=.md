---
title: "CSimpleStringT::operator ="
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
ms.assetid: c12b2883-1673-4304-ad12-0e65571a6a8a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::operator =
Assigns a new value to a `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      CSimpleStringT& operator =(  
   PCXSTR pszSrc   
);  
CSimpleStringT& operator =(  
   const CSimpleStringT& strSrc   
);  
```  
  
#### Parameters  
 `pszSrc`  
 A pointer to a null-terminated string.  
  
 `strSrc`  
 A pointer to an existing `CSimpleStringT` object.  
  
## Remarks  
 If the destination string (the left side) is already large enough to store the new data, no new memory allocation is performed. Note that memory exceptions may occur whenever you use the assignment operator because new storage is often allocated to hold the resulting `CSimpleStringT` object.  
  
## Example  
 The following example demonstrates the use of **CSimpleStringT::operator =**.  
  
 [!CODE [NVC_ATLMFC_Utilities#94](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#94)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::CSimpleStringT](../vs140/CSimpleStringT--CSimpleStringT.md)