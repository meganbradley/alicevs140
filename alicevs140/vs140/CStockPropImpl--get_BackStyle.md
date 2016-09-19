---
title: "CStockPropImpl::get_BackStyle"
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
ms.assetid: 4e07ccea-2860-47d4-9b08-febb3e8c78da
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_BackStyle
Call this method to get the control's background style, either transparent or opaque.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_BackStyle(  
   LONG * pnBackStyle  
);  
```  
  
#### Parameters  
 *pnBackStyle*  
 Variable that receives the control's background style.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_BackStyle](../vs140/CStockPropImpl--put_BackStyle.md)