---
title: "CComBSTR::Length"
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
ms.assetid: a2701c46-f3b2-497b-a68c-ecbacc1715ff
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::Length
Returns the number of characters in `m_str`, excluding the terminating null character.  
  
## Syntax  
  
```  
  
unsigned int Length( ) const throw( );  
  
```  
  
## Return Value  
 The length of the [m_str](../vs140/CComBSTR--m_str.md) member.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#42](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#42)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)