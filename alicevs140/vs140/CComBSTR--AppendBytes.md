---
title: "CComBSTR::AppendBytes"
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
ms.assetid: 6ea412f3-2f9d-415a-a23d-c6d17f625794
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::AppendBytes
Appends the specified number of bytes to [m_str](../vs140/CComBSTR--m_str.md) without conversion.  
  
## Syntax  
  
```  
  
      HRESULT AppendBytes(  
   const char* lpsz,  
   int nLen  
) throw( );  
```  
  
#### Parameters  
 `lpsz`  
 [in] A pointer to an array of bytes to append.  
  
 `p`  
 [in] The number of bytes to append.  
  
## Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#34](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#34)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::Append](../vs140/CComBSTR--Append.md)   
 [CComBSTR::operator +=](../vs140/CComBSTR--operator--=.md)   
 [CComBSTR::operator +=](../vs140/CComBSTR--operator--=.md)