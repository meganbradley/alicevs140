---
title: "CStringT::CompareNoCase"
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
ms.assetid: 06476696-a2d4-4192-9935-44721f1dcedc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::CompareNoCase
Compares two strings (case insensitive).  
  
## Syntax  
  
```  
int CompareNoCase(  
   PCXSTR psz  
) const throw();  
```  
  
#### Parameters  
 `psz`  
 The other string used for comparison.  
  
## Return Value  
 Zero if the strings are identical (ignoring case), <0 if this `CStringT` object is less than `psz` (ignoring case), or >0 if this `CStringT` object is greater than `psz` (ignoring case).  
  
## Remarks  
 The generic-text function `_tcsicmp`, which is defined in TCHAR.H, maps to either `_stricmp`, `_wcsicmp` or `_mbsicmp`, depending on the character set that is defined at compile time. Each function performs a case-insensitive comparison of the strings. The comparison depends on the `LC_CTYPE` aspect of the locale but not `LC_COLLATE`. For more information, see [_stricmp, _wcsicmp, _mbsicmp, _stricmp_l, _wcsicmp_l, _mbsicmp_l](../vs140/_stricmp--_wcsicmp--_mbsicmp--_stricmp_l--_wcsicmp_l--_mbsicmp_l.md).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#111](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#111)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)