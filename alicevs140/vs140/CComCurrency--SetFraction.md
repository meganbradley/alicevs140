---
title: "CComCurrency::SetFraction"
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
ms.assetid: 5c9491cb-dd83-4ade-b496-b48b4d97542f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::SetFraction
Call this method to set the fractional component of a `CComCurrency` object.  
  
## Syntax  
  
```  
  
      HRESULT SetFraction(  
   SHORT nFraction   
);  
```  
  
#### Parameters  
 *nFraction*  
 The value to be assigned to the fractional component of the `m_currency` data member. The sign of the fractional component must the same as the integer component, and the value must be in range -9999 (**CY_MIN_FRACTION**) to +9999 (**CY_MAX_FRACTION**).  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#53](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#53)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::GetFraction](../vs140/CComCurrency--GetFraction.md)   
 [CComCurrency::SetInteger](../vs140/CComCurrency--SetInteger.md)   
 [CComCurrency::SetInteger](../vs140/CComCurrency--SetInteger.md)