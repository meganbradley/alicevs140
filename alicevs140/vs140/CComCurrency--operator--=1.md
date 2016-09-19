---
title: "CComCurrency::operator -=1"
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
H1: CComCurrency::operator -=
ms.assetid: f826a7f1-d6bb-4495-a31a-513a1e2e6b3f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::operator -=1
This operator is used to perform subtraction on a `CComCurrency` object and assign it the result.  
  
## Syntax  
  
```  
  
      const CComCurrency & operator -=(  
   const CComCurrency & cur   
);  
```  
  
#### Parameters  
 `cur`  
 A `CComCurrency` object.  
  
## Return Value  
 Returns the updated `CComCurrency` object. In the event of an error, such as an overflow, this operator calls `AtlThrow` with an HRESULT describing the error.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#66](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#66)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::operator -](../vs140/CComCurrency--operator--2.md)   
 [CComCurrency::operator +](../vs140/CComCurrency--operator--.md)   
 [CComCurrency::operator *](../vs140/CComCurrency--operator--.md)   
 [CComCurrency::operator /](../vs140/CComCurrency--operator--1.md)