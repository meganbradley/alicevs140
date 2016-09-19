---
title: "CStringT::Format"
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
ms.assetid: 6fa4ea8f-9957-4aa6-b242-5abfa524c0a9
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::Format
Writes formatted data to a `CStringT` in the same way that [sprintf_s](../vs140/sprintf_s--_sprintf_s_l--swprintf_s--_swprintf_s_l.md) formats data into a C-style character array.  
  
## Syntax  
  
```  
void __cdecl Format(  
   UINT nFormatID,  
   [, argument]...  
);  
void __cdecl Format(  
   PCXSTR pszFormat,  
   [, argument]...  
);  
```  
  
#### Parameters  
 `nFormatID`  
 The string resource identifier that contains the format-control string.  
  
 `pszFormat`  
 A format-control string.  
  
 `argument`  
 Optional arguments.  
  
## Remarks  
 This function formats and stores a series of characters and values in the `CStringT`. Each optional argument (if any) is converted and output according to the corresponding format specification in `pszFormat` or from the string resource identified by `nFormatID`.  
  
 The call will fail if the string object itself is offered as a parameter to `Format`. For example, the following code will cause unpredictable results:  
  
 [!CODE [NVC_ATLMFC_Utilities#116](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#116)]  
  
 For more information, see [Format Specification Syntax: printf and wprintf Functions](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#117](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#117)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)   
 [sprintf_s, _sprintf_s_l, swprintf_s, _swprintf_s_l](../vs140/sprintf_s--_sprintf_s_l--swprintf_s--_swprintf_s_l.md)