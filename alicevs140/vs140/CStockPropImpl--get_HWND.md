---
title: "CStockPropImpl::get_HWND"
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
ms.assetid: ebc24ea2-6f03-4bfb-8260-f474958bfc4e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::get_HWND
Call this method to get the window handle associated with the control.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE get_HWND(  
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
 [CStockPropImpl::put_HWND](../vs140/CStockPropImpl--put_HWND.md)