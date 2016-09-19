---
title: "CComVariant::operator &lt;"
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
ms.assetid: 8b241434-6aa2-4f0e-9be1-d621c77d04f7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComVariant::operator &lt;
Indicates whether the `CComVariant` object is less than the specified **VARIANT**.  
  
## Syntax  
  
```  
  
      bool operator <(  
   const VARIANT& varSrc   
) const throw();  
```  
  
## Remarks  
 Returns **true** if the value of the `CComVariant` object is less than the value of *varSrc*. Otherwise, **false**. The operator uses the user's default locale to perform the comparison.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComVariant Class](../vs140/CComVariant-Class.md)   
 [CComVariant::operator >](../vs140/CComVariant--operator--.md)   
 [VARIANT](assetId:///e305240e-9e11-4006-98cc-26f4932d2118)