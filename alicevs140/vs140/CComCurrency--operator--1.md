---
title: "CComCurrency::operator -1"
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
H1: CComCurrency::operator /
ms.assetid: 59fe428d-f3a7-4caf-a420-c606409607b7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::operator -1
This operator is used to perform division on a `CComCurrency` object.  
  
## Syntax  
  
```  
  
      CComCurrency operator /(  
   long nOperand   
) const;  
```  
  
#### Parameters  
 `nOperand`  
 The divisor.  
  
## Return Value  
 Returns a `CComCurrency` object representing the result of the division. If the divisor is 0, an assert failure will occur.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#59](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#59)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)   
 [CComCurrency::operator /=](../vs140/CComCurrency--operator--=2.md)   
 [CComCurrency::operator +](../vs140/CComCurrency--operator--.md)   
 [CComCurrency::operator -](../vs140/CComCurrency--operator--2.md)   
 [CComCurrency::operator *](../vs140/CComCurrency--operator--.md)