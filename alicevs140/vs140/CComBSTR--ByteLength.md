---
title: "CComBSTR::ByteLength"
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
ms.assetid: c0dd0da0-bfc6-4ac6-b5b9-5d0fe2af4a3c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::ByteLength
Returns the number of bytes in `m_str`, excluding the terminating null character.  
  
## Syntax  
  
```  
  
unsigned int ByteLength( ) const throw( );  
  
```  
  
## Return Value  
 The length of the [m_str](../vs140/CComBSTR--m_str.md) member in bytes.  
  
## Remarks  
 Returns 0 if `m_str` is **NULL**.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#36](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#36)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::Length](../vs140/CComBSTR--Length.md)