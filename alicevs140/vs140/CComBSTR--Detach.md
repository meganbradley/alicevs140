---
title: "CComBSTR::Detach"
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
ms.assetid: 9e914c0b-8c30-4030-8b78-61be3d10b0bc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::Detach
Detaches [m_str](../vs140/CComBSTR--m_str.md) from the `CComBSTR` object and sets `m_str` to **NULL**.  
  
## Syntax  
  
```  
  
BSTR Detach( ) throw( );  
  
```  
  
## Return Value  
 The `BSTR` associated with the `CComBSTR` object.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#40](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#40)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::Attach](../vs140/CComBSTR--Attach.md)