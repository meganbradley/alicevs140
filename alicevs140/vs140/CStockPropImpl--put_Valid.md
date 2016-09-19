---
title: "CStockPropImpl::put_Valid"
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
ms.assetid: 6ac432b7-cabd-49cd-bac4-85c60dbacc78
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_Valid
Call this method to set the flag that indicates if the control is valid or not.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Valid(   
   VARIANT_BOOL bValid  
);  
```  
  
#### Parameters  
 *bValid*  
 TRUE if the control is valid.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_Valid](../vs140/CStockPropImpl--get_Valid.md)