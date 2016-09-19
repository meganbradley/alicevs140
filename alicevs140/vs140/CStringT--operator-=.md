---
title: "CStringT::operator ="
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
ms.assetid: 190f699b-9e52-4c5a-b9b2-9ed58febc1c6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::operator =
The `CStringT` assignment (`=`) operator reinitializes an existing `CStringT` object with new data.  
  
## Syntax  
  
```  
CString& operator=(  
   const VARIANT& var  
);  
CString& operator=(  
   wchar_t ch  
);  
CString& operator=(  
   char ch  
);  
CString& operator=(  
   const unsigned char* pszSrc  
);  
CString& operator=(  
   PCYSTR pszSrc  
);  
CString& operator=(  
   PCXSTR pszSrc  
);  
template <bool bMFCDLL>  
CString& operator=(  
   const CSimpleStringT<BaseType, bMFCDLL>& strSrc  
);  
CString& operator=(  
   const CStringT& strSrc  
);  
```  
  
#### Parameters  
 `var`  
 A variant-type object to be copied into this `CStringT` object.  
  
 `ch`  
 A single character.  
  
 `strSrc`  
 A null-terminated string to be copied into this `CStringT` object.  
  
 `pszSrc`  
 A `CStringT` to be copied into this `CStringT`object.  
  
## Remarks  
 If the destination string (that is, the left side) is already large enough to store the new data, no new memory allocation is performed. You should be aware that memory exceptions can occur whenever you use the assignment operator because new storage is often allocated to hold the resulting `CStringT` object.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#139](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#139)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)