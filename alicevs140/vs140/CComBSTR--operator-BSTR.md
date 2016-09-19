---
title: "CComBSTR::operator BSTR"
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
ms.assetid: 111cf620-cae9-47e5-9610-e00125db7a83
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::operator BSTR
Casts a `CComBSTR` object to a `BSTR`.  
  
## Syntax  
  
```  
  
operator BSTR( ) const throw( );  
  
```  
  
## Remarks  
 Allows you to pass `CComBSTR` objects to functions that have **[in] BSTR** parameters.  
  
## Example  
 See the example for [CComBSTR::m_str](../vs140/CComBSTR--m_str.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)