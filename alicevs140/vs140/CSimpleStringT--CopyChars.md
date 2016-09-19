---
title: "CSimpleStringT::CopyChars"
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
ms.assetid: eef6bc57-eb2a-4dd7-aa3e-5af8861baaf5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::CopyChars
Copies a character or characters to a `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      static void CopyChars(  
   XCHAR* pchDest,  
   const XCHAR* pchSrc,  
   int nChars  
) throw( );  
```  
  
#### Parameters  
 `pchDest`  
 A pointer to a character string.  
  
 `pchSrc`  
 A pointer to a string containing the characters to be copied.  
  
 `nChars`  
 The number of `pchSrc` characters to be copied.  
  
## Remarks  
 Call this method to copy characters from `pchSrc` to the `pchDest` string.  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::CopyChars`.  
  
 [!CODE [NVC_ATLMFC_Utilities#76](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#76)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)