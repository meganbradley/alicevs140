---
title: "CComBSTR::operator &amp;"
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
ms.assetid: 143ad1cf-d83e-4d6d-806e-a04a1712c857
caps.latest.revision: 28
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::operator &amp;
Returns the address of the `BSTR` stored in the [m_str](../vs140/CComBSTR--m_str.md) member.  
  
## Syntax  
  
```  
BSTR* operator &( ) throw( );  
```  
  
## Remarks  
 `CComBstr operator &` has a special assertion associated with it to help identify memory leaks. The program will assert when the `m_str` member is initialized. This assertion was created to identify situations where a programmer uses the `& operator` to assign a new value to `m_str` member without freeing the first allocation of `m_str`. If `m_str` equals NULL, the program assumes that m_str wasn't allocated yet. In this case, the program will not assert.  
  
 This assertion is not enabled by default. Define `ATL_CCOMBSTR_ADDRESS_OF_ASSERT` to enable this assertion.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#46](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#46)]  
  
 [!CODE [NVC_ATL_Utilities#47](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#47)]  
  
## Requirements  
 `Header:` atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)