---
title: "CStockPropImpl::put_Enabled"
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
ms.assetid: f7decc67-1e70-4055-9138-2e31df38d905
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_Enabled
Call this method to set the value of the flag that indicates if the control is enabled.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_Enabled(  
   VARIANT_BOOL bEnabled  
);  
```  
  
#### Parameters  
 `bEnabled`  
 TRUE if the control is enabled.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_Enabled](../vs140/CStockPropImpl--get_Enabled.md)