---
title: "CComBSTR::AppendBSTR"
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
ms.assetid: f8edd475-921b-4652-8b78-f8475c49b233
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::AppendBSTR
Appends the specified `BSTR` to [m_str](../vs140/CComBSTR--m_str.md).  
  
## Syntax  
  
```  
  
      HRESULT AppendBSTR(  
   BSTR p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 [in] A `BSTR` to append.  
  
## Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
## Remarks  
 Do not pass an ordinary wide-character string to this method. The compiler cannot catch the error and run time errors will occur.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#33](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#33)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::Append](../vs140/CComBSTR--Append.md)   
 [CComBSTR::operator +=](../vs140/CComBSTR--operator--=.md)   
 [ATL and MFC String Conversion Macros](../vs140/ATL-and-MFC-String-Conversion-Macros.md)