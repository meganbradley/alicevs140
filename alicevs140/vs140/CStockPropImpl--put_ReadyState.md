---
title: "CStockPropImpl::put_ReadyState"
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
ms.assetid: 36c56355-3ee4-4e43-ac1d-c97e671570a1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_ReadyState
Call this method to set the control's ready state, for example, loading or loaded.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_ReadyState(  
   LONG nReadyState  
);  
```  
  
#### Parameters  
 *nReadyState*  
 The control's ready state.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_ReadyState](../vs140/CStockPropImpl--get_ReadyState.md)