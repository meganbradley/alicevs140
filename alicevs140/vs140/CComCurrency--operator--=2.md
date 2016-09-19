---
title: "CComCurrency::operator -=2"
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
H1: CComCurrency::operator /=
ms.assetid: 41ad5f89-b795-40f0-94c9-6792d3487712
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::operator -=2
This operator is used to perform division on a `CComCurrency` object and assign it the result.  
  
## Syntax  
  
```  
  
      const CComCurrency & operator /=(  
   long nOperand   
);  
```  
  
#### Parameters  
 `nOperand`  
 The divisor.  
  
## Return Value  
 Returns the updated `CComCurrency` object. If the divisor is 0, an assert failure will occur.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#60](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#60)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::operator /](../vs140/CComCurrency--operator--1.md)   
 [CComCurrency::operator +](../vs140/CComCurrency--operator--.md)   
 [CComCurrency::operator -](../vs140/CComCurrency--operator--2.md)   
 [CComCurrency::operator *](../vs140/CComCurrency--operator--.md)