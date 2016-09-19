---
title: "CComBSTR::operator ="
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
ms.assetid: 20adbef8-056c-4a2f-92f8-fb8645bef9ee
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::operator =
Sets the [m_str](../vs140/CComBSTR--m_str.md) member to a copy of `pSrc` or to a copy of the `BSTR` member of *src*.  
  
## Syntax  
  
```  
  
      CComBSTR& operator =(  
   const CComBSTR& src   
);  
CComBSTR& operator =(  
   LPCOLESTR pSrc   
);  
CComBSTR& operator =(  
   LPCSTR pSrc   
);  
```  
  
## Remarks  
 The `pSrc` parameter specifies either an **LPCOLESTR** for Unicode versions or `LPCSTR` for ANSI versions.  
  
## Example  
 See the example for [CComBSTR::Copy](../vs140/CComBSTR--Copy.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::Copy](../vs140/CComBSTR--Copy.md)