---
title: "CComBSTR::operator !"
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
ms.assetid: 69d9b881-cce4-4003-b3ab-34b5b47f0067
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::operator !
Checks whether `BSTR` string is NULL.  
  
## Syntax  
  
```  
  
bool operator !( ) const throw( );  
  
```  
  
## Return Value  
 Returns **true** if the [m_str](../vs140/CComBSTR--m_str.md) member is **NULL**; otherwise, **false**.  
  
## Remarks  
 This operator only checks for a NULL value, not for an empty string.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#35](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#35)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)