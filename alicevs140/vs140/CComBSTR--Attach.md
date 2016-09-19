---
title: "CComBSTR::Attach"
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
ms.assetid: 1ecb7183-5a01-428d-b8a1-c13af795ecf8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::Attach
Attaches a `BSTR` to the `CComBSTR` object by setting the [m_str](../vs140/CComBSTR--m_str.md) member to *src*.  
  
## Syntax  
  
```  
  
      void Attach(  
   BSTR src   
) throw( );  
```  
  
#### Parameters  
 *src*  
 [in] The `BSTR` to attach to the object.  
  
## Remarks  
 Do not pass an ordinary wide-character string to this method. The compiler cannot catch the error and run time errors will occur.  
  
> [!NOTE]
>  This method will assert if `m_str` is non-**NULL**.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#35](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#35)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::Detach](../vs140/CComBSTR--Detach.md)   
 [CComBSTR::operator =](../vs140/CComBSTR--operator-=.md)