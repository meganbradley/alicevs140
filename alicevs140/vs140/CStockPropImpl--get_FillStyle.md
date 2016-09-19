---
title: "CStockPropImpl::get_FillStyle"
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
ms.assetid: 567fa467-2fe7-4a38-ae2d-cf52ca6754e9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_FillStyle
Call this method to get the control's fill style, for example, solid, transparent, or crosshatched.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_FillStyle(  
   LONG * pnFillStyle  
);  
```  
  
#### Parameters  
 *pnFillStyle*  
 Variable that receives the control's fill style.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_FillStyle](../vs140/CStockPropImpl--put_FillStyle.md)