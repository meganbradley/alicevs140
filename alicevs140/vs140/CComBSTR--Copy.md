---
title: "CComBSTR::Copy"
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
ms.assetid: b53b57c4-b078-40ea-a48c-99521ca5e73b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::Copy
Allocates and returns a copy of `m_str`.  
  
## Syntax  
  
```  
  
BSTR Copy( ) const throw();  
  
```  
  
## Return Value  
 A copy of the [m_str](../vs140/CComBSTR--m_str.md) member. If `m_str` is **NULL**, returns **NULL**.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#38](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#38)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::CopyTo](../vs140/CComBSTR--CopyTo.md)   
 [CComBSTR::operator =](../vs140/CComBSTR--operator-=.md)