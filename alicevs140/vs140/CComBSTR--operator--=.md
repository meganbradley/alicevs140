---
title: "CComBSTR::operator +="
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
ms.assetid: 7383d7c2-f58e-4c18-8a57-17e5b1a3ca74
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::operator +=
Appends a string to the `CComBSTR` object.  
  
## Syntax  
  
```  
  
      CComBSTR& operator +=(  
   const CComBSTR& bstrSrc   
);  
CComBSTR& operator +=(  
   const LPCOLESTR pszSrc   
);  
```  
  
#### Parameters  
 `bstrSrc`  
 [in] A `CComBSTR` object to append.  
  
 `pszSrc`  
 [in] A zero-terminated string to append.  
  
## Remarks  
 `CComBSTR`s are compared textually in the context of the user's default locale. The **LPCOLESTR** comparison is done using `memcmp` on the raw data in each string. The `LPCSTR` comparison is carried out in the same way once a temporary Unicode copy of `pszSrc` has been created. The final comparison operator just compares the contained string against **NULL**.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#48](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#48)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::Append](../vs140/CComBSTR--Append.md)   
 [CComBSTR::AppendBSTR](../vs140/CComBSTR--AppendBSTR.md)   
 [ATL and MFC String Conversion Macros](../vs140/ATL-and-MFC-String-Conversion-Macros.md)