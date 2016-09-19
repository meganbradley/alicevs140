---
title: "CStockPropImpl::put_DrawMode"
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
ms.assetid: fd455fd3-cb8a-4a99-a04f-4b5e65ff020d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_DrawMode
Call this method to set the control's drawing mode, for example, XOR Pen or Invert Colors.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_DrawMode(  
   LONG nDrawMode  
);  
```  
  
#### Parameters  
 `nDrawMode`  
 The new drawing mode for the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_DrawMode](../vs140/CStockPropImpl--get_DrawMode.md)