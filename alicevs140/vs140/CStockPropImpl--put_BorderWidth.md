---
title: "CStockPropImpl::put_BorderWidth"
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
ms.assetid: 8ef34377-dff0-4286-8b49-b8a773198285
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_BorderWidth
Call this method to set the width of the control's border.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_BorderWidth(  
   LONG nBorderWidth  
);  
```  
  
#### Parameters  
 `nBorderWidth`  
 The new width of the control's border.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_BorderWidth](../vs140/CStockPropImpl--get_BorderWidth.md)