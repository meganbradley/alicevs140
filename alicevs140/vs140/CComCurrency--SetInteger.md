---
title: "CComCurrency::SetInteger"
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
ms.assetid: b1adea0e-8f60-4e7e-bf9e-a1e67ed60645
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::SetInteger
Call this method to set the integer component of a `CComCurrency` object.  
  
## Syntax  
  
```  
  
      HRESULT SetInteger(  
   LONGLONG nInteger   
);  
```  
  
#### Parameters  
 `nInteger`  
 The value to be assigned to the integer component of the `m_currency` data member. The sign of the integer component must match the sign of the existing fractional component.  
  
 `nInteger` must be in the range **CY_MIN_INTEGER** to **CY_MAX_INTEGER** inclusive. These values are defined in atlcur.h.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#54](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#54)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::GetInteger](../vs140/CComCurrency--GetInteger.md)   
 [CComCurrency::GetFraction](../vs140/CComCurrency--GetFraction.md)   
 [CComCurrency::SetFraction](../vs140/CComCurrency--SetFraction.md)