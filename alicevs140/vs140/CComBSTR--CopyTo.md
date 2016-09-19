---
title: "CComBSTR::CopyTo"
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
ms.assetid: 8e687b1b-7c63-4b2b-a056-e0392282c80e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::CopyTo
Allocates and returns a copy of [m_str](../vs140/CComBSTR--m_str.md) via the parameter.  
  
## Syntax  
  
```  
  
      HRESULT CopyTo(  
   BSTR* pbstr   
) throw( );  
HRESULT CopyTo(  
   VARIANT* pvarDest   
) throw( );  
```  
  
#### Parameters  
 *pbstr*  
 [out] The address of a `BSTR` in which to return the string allocated by this method.  
  
 `pvarDest`  
 [out] The address of a **VARIANT** in which to return the string allocated by this method.  
  
## Return Value  
 A standard `HRESULT` value indicating the success or failure of the copy.  
  
## Remarks  
 After calling this method, the **VARIANT** pointed to by `pvarDest` will be of type `VT_BSTR`.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#39](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#39)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::Copy](../vs140/CComBSTR--Copy.md)   
 [CComBSTR::operator =](../vs140/CComBSTR--operator-=.md)