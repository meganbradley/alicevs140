---
title: "CStockPropImpl::get_ReadyState"
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
ms.assetid: 528085c0-7ddc-45f0-97cf-44d7767e5ee3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_ReadyState
Call this method to get the control's ready state, for example, loading or loaded.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_ReadyState(  
   LONG * pnReadyState  
);  
```  
  
#### Parameters  
 *pnReadyState*  
 Variable that receives the control's ready state.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_ReadyState](../vs140/CStockPropImpl--put_ReadyState.md)