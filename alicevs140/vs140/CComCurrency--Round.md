---
title: "CComCurrency::Round"
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
ms.assetid: f0a11a5a-50af-4149-b167-8e138c9a4332
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::Round
Call this method to round the currency to a specified number of decimal places.  
  
## Syntax  
  
```  
  
      HRESULT Round(  
   int nDecimals   
);  
```  
  
#### Parameters  
 *nDecimals*  
 The number of digits to which `m_currency` will be rounded, in the range 0 to 4.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#52](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#52)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)