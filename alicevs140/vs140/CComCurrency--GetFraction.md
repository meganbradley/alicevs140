---
title: "CComCurrency::GetFraction"
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
ms.assetid: a9fad4ab-41c0-4e6d-9b90-667cf3870e6b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::GetFraction
Call this method to return the fractional component of the `CComCurrency` object.  
  
## Syntax  
  
```  
  
SHORT GetFraction( ) const;  
  
```  
  
## Return Value  
 Returns the fractional component of the `m_currency` data member.  
  
## Remarks  
 The fractional component is a 4-digit integer value between -9999 (**CY_MIN_FRACTION**) and +9999 (**CY_MAX_FRACTION**). `GetFraction` returns this value scaled by 10000 (**CY_SCALE**). The values of **CY_MIN_FRACTION**, **CY_MAX_FRACTION**, and **CY_SCALE** are defined in atlcur.h.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#50](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#50)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::SetFraction](../vs140/CComCurrency--SetFraction.md)   
 [CComCurrency::GetInteger](../vs140/CComCurrency--GetInteger.md)   
 [CComCurrency::SetInteger](../vs140/CComCurrency--SetInteger.md)