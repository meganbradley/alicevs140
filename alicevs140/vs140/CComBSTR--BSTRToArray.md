---
title: "CComBSTR::BSTRToArray"
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
ms.assetid: 8dc75600-e196-4e6e-96b6-c005315ea52d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::BSTRToArray
Creates a zero-based one-dimensional safearray, where each element of the array is a character from the `CComBSTR` object.  
  
## Syntax  
  
```  
  
      HRESULT BSTRToArray(  
   LPSAFEARRAY* ppArray   
) throw( );  
```  
  
#### Parameters  
 `ppArray`  
 [out] The pointer to the safearray used to hold the results of the function.  
  
## Return Value  
 `S_OK` on success, or any standard `HRESULT` error value.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)