---
title: "CComCurrency::operator +="
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
ms.assetid: 18047ca7-1717-4cfa-b09e-6c1a5d5ed871
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::operator +=
This operator is used to perform addition on a `CComCurrency` object and assign the result to the current object.  
  
## Syntax  
  
```  
  
      const CComCurrency & operator +=(  
   const CComCurrency & cur   
);  
```  
  
#### Parameters  
 `cur`  
 The `CComCurrency` object.  
  
## Return Value  
 Returns the updated `CComCurrency` object. In the event of an error, such as an overflow, this operator calls `AtlThrow` with an HRESULT describing the error.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#62](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#62)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::operator *=](../vs140/CComCurrency--operator--=.md)   
 [CComCurrency::operator +](../vs140/CComCurrency--operator--.md)   
 [CComCurrency::operator -](../vs140/CComCurrency--operator--2.md)   
 [CComCurrency::operator /](../vs140/CComCurrency--operator--1.md)