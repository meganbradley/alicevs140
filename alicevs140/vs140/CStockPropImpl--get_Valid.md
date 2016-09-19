---
title: "CStockPropImpl::get_Valid"
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
ms.assetid: d9ad0455-1870-44f8-9f9b-3c5e83513c00
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_Valid
Call this method to get the status of the flag that indicates if the control is valid or not.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Valid(   
   VARIANT_BOOL * pbValid  
);  
```  
  
#### Parameters  
 *pbValid*  
 Variable that receives the flag status. TRUE indicates that the control is valid.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Valid](../vs140/CStockPropImpl--put_Valid.md)