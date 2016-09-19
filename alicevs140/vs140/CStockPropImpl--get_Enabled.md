---
title: "CStockPropImpl::get_Enabled"
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
ms.assetid: d0a74d8f-718a-4b3f-8a17-cd465577140e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_Enabled
Call this method to get the status of the flag that indicates if the control is enabled.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Enabled(  
   VARIANT_BOOL * pbEnabled  
);  
```  
  
#### Parameters  
 `pbEnabled`  
 Variable that receives the flag status. TRUE indicates that the control is enabled.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Enabled](../vs140/CStockPropImpl--put_Enabled.md)