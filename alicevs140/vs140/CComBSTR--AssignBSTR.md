---
title: "CComBSTR::AssignBSTR"
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
ms.assetid: 243c843f-4f2f-4b4f-a0fd-fcc8dcaecbdc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::AssignBSTR
Assigns a `BSTR` to [m_str](../vs140/CComBSTR--m_str.md).  
  
## Syntax  
  
```  
  
      HRESULT AssignBSTR(  
   const BSTR bstrSrc   
) throw( );  
```  
  
#### Parameters  
 `bstrSrc`  
 [in] A `BSTR` to assign to the current `CComBSTR` object.  
  
## Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)