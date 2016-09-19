---
title: "CStockPropImpl::get_DrawStyle"
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
ms.assetid: 06c55097-1933-4b5c-bc82-65217f0ec92e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_DrawStyle
Call this method to get the control's drawing style, for example, solid, dashed, or dotted.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_DrawStyle(  
   LONG * pnDrawStyle  
);  
```  
  
#### Parameters  
 *pnDrawStyle*  
 Variable that receives the control's drawing style.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_DrawStyle](../vs140/CStockPropImpl--put_DrawStyle.md)