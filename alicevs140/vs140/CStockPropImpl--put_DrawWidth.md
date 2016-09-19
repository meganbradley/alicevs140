---
title: "CStockPropImpl::put_DrawWidth"
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
ms.assetid: 27b92048-2e72-4256-8018-2315aa34fb54
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_DrawWidth
Call this method to set the width (in pixels) used by the control's drawing methods.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_DrawWidth(  
   LONG nDrawWidth  
);  
```  
  
#### Parameters  
 *nDrawWidth*  
 The new width to be used by the control's drawing methods.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_DrawWidth](../vs140/CStockPropImpl--get_DrawWidth.md)