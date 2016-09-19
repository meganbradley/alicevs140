---
title: "CStockPropImpl::put_BackStyle"
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
ms.assetid: 75589b7b-4cdd-4ecb-bae8-d0864b087f1e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_BackStyle
Call this method to set the control's background style.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_BackStyle(  
   LONG nBackStyle  
);  
```  
  
#### Parameters  
 *nBackStyle*  
 The new control background style.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_BackStyle](../vs140/CStockPropImpl--get_BackStyle.md)