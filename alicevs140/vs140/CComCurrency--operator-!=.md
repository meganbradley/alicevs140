---
title: "CComCurrency::operator !="
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
ms.assetid: d1776841-b1c9-4fcc-bbc5-5e7df27d06d6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::operator !=
This operator compares two objects for inequality.  
  
## Syntax  
  
```  
  
      bool operator !=(  
   const CComCurrency & cur   
) const;  
```  
  
#### Parameters  
 `cur`  
 The `CComCurrency` object to be compared.  
  
## Return Value  
 Returns **true** if the item being compared is not equal to the `CComCurrency` object; otherwise, **false**.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#56](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#56)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::operator ==](../vs140/CComCurrency--operator-==.md)