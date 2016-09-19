---
title: "CComCurrency::operator =="
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
ms.assetid: 2ad9bb56-5e9d-4696-aa66-1f4a767c4b51
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::operator ==
This operator compares two `CComCurrency` objects for equality.  
  
## Syntax  
  
```  
  
      bool operator ==(  
   const CComCurrency & cur   
) const;  
```  
  
#### Parameters  
 `cur`  
 The `CComCurrency` object to compare.  
  
## Return Value  
 Returns **true** if the objects are equal (that is, the `m_currency` data members, both integer and fractional, in both objects have the same value), **false** otherwise.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#67](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#67)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::operator !=](../vs140/CComCurrency--operator-!=.md)