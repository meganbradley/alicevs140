---
title: "CStockPropImpl::put_DrawStyle"
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
ms.assetid: 83f130ee-a7d2-47b5-a087-910e43007d7a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_DrawStyle
Call this method to set the control's drawing style, for example, solid, dashed, or dotted.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_DrawStyle(  
   LONG pnDrawStyle  
);  
```  
  
#### Parameters  
 *nDrawStyle*  
 The new drawing style for the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_DrawStyle](../vs140/CStockPropImpl--get_DrawStyle.md)