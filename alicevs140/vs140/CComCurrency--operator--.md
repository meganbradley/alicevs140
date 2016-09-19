---
title: "CComCurrency::operator &gt;"
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
ms.assetid: 29d4d42c-b503-4bb0-a64e-f2918c8af208
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::operator &gt;
This operator compares two `CComCurrency` objects to determine the larger.  
  
## Syntax  
  
```  
  
      bool operator >(  
   const CComCurrency & cur   
) const;  
```  
  
#### Parameters  
 `cur`  
 A `CComCurrency` object.  
  
## Return Value  
 Returns **true** if the first object is greater than the second, **false** otherwise.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#68](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#68)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::operator >=](../vs140/CComCurrency--operator--=.md)   
 [CComCurrency::operator <](../vs140/CComCurrency--operator--.md)   
 [CComCurrency::operator <=](../vs140/CComCurrency--operator--=.md)