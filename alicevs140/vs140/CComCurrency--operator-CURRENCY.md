---
title: "CComCurrency::operator CURRENCY"
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
ms.assetid: d179aa03-eb83-4681-9f93-a8c75c0209a4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCurrency::operator CURRENCY
These operators are used to cast a `CComCurrency` object to a **CURRENCY** data type.  
  
## Syntax  
  
```  
  
      operator CURRENCY&( ) throw( );   
operator const CURRENCY&( ) const throw( );  
```  
  
## Return Value  
 Returns a reference to a **CURRENCY** object.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#70](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#70)]  
  
## Requirements  
 **Header:** atlcur.h  
  
## See Also  
 [CComCurrency Class](../vs140/CComCurrency-Class.md)