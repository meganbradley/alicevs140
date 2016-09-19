---
title: "CComBSTR::ArrayToBSTR"
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
ms.assetid: 27b5fb73-5592-4587-825d-ddfcfef1112f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::ArrayToBSTR
Frees any existing string held in the `CComBSTR` object, then creates a `BSTR` from the first character of each element in the safearray and attaches it to the `CComBSTR` object.  
  
## Syntax  
  
```  
  
      HRESULT ArrayToBSTR(  
   const SAFEARRAY* pSrc   
) throw( );  
```  
  
#### Parameters  
 `pSrc`  
 [in] The safearray containing the elements used to create the string.  
  
## Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)