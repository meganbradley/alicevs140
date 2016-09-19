---
title: "CComCurrency::GetInteger"
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
ms.assetid: e3aa4c45-d25a-4b3c-a6f0-1a952d83a69f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::GetInteger
Call this method to get the integer component of a `CComCurrency` object.  
  
## Syntax  
  
```  
  
LONGLONG GetInteger( ) const;  
  
```  
  
## Return Value  
 Returns the integer component of the `m_currency` data member.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#51](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#51)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::SetInteger](../vs140/CComCurrency--SetInteger.md)   
 [CComCurrency::GetFraction](../vs140/CComCurrency--GetFraction.md)   
 [CComCurrency::SetFraction](../vs140/CComCurrency--SetFraction.md)