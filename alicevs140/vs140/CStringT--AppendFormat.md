---
title: "CStringT::AppendFormat"
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
ms.assetid: c686fd78-8b44-4411-b90d-2f2581fe2f2f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::AppendFormat
Appends formatted data to an existing `CStringT` object.  
  
## Syntax  
  
```  
void __cdecl AppendFormat(  
   PCXSTR pszFormat,  
   [, argument]...  
);  
void __cdecl AppendFormat(  
   UINT nFormatID,  
   [, argument]...  
);  
```  
  
#### Parameters  
 `pszFormat`  
 A format-control string.  
  
 `nFormatID`  
 The string resource identifier that contains the format-control string.  
  
 `argument`  
 Optional arguments.  
  
## Remarks  
 This function formats and appends a series of characters and values in the `CStringT`. Each optional argument (if any) is converted and appended according to the corresponding format specification in `pszFormat` or from the string resource identified by `nFormatID`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#107](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#107)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)