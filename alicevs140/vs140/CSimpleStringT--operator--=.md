---
title: "CSimpleStringT::operator +="
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
ms.assetid: c45c53e5-a4d6-45fb-a49f-9484fd61d96d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::operator +=
Joins a new string or character to the end of an existing string.  
  
## Syntax  
  
```  
  
      CSimpleStringT& operator +=(  
   PCXSTR pszSrc   
);  
CSimpleStringT& operator +=(  
   const CSimpleStringT& strSrc   
);  
template< int t_nSize >  
CSimpleStringT& operator+=(  
   const CStaticString< XCHAR, t_nSize >& strSrc  
);  
CSimpleStringT& operator +=(  
   char ch   
);  
CSimpleStringT& operator +=(  
   unsigned char ch   
);  
CSimpleStringT& operator +=(  
   wchar_t ch   
);  
```  
  
#### Parameters  
 `pszSrc`  
 A pointer to a null-terminated string.  
  
 `strSrc`  
 A pointer to an existing `CSimpleStringT` object.  
  
 *ch*  
 The character to be appended.  
  
## Remarks  
 The operator accepts another `CSimpleStringT` object or a character. Note that memory exceptions may occur whenever you use this concatenation operator because new storage may be allocated for characters added to this `CSimpleStringT` object.  
  
## Example  
 The following example demonstrates the use of **CSimpleStringT::operator +=**.  
  
 [!CODE [NVC_ATLMFC_Utilities#93](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#93)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)