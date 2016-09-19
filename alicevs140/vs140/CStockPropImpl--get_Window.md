---
title: "CStockPropImpl::get_Window"
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
ms.assetid: c7ee8cfa-619c-4dc8-9c64-08e3a17674b0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_Window
Call this method to get the window handle associated with the control. Identical to [CStockPropImpl::get_HWND](../vs140/CStockPropImpl--get_HWND.md).  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_Window(  
   LONG_PTR* phWnd   
);  
```  
  
#### Parameters  
 `phWnd`  
 The window handle associated with the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::put_Window](../vs140/CStockPropImpl--put_Window.md)