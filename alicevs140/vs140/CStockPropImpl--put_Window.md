---
title: "CStockPropImpl::put_Window"
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
ms.assetid: 317ad228-fea2-45fb-8fe9-de040cd6068f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStockPropImpl::put_Window
This method calls [CStockPropImpl::put_HWND](../vs140/CStockPropImpl--put_HWND.md), which returns E_FAIL.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE put_Window(  
   LONG_PTR hWnd   
);  
```  
  
#### Parameters  
 `hWnd`  
 The window handle.  
  
## Return Value  
 Returns E_FAIL.  
  
## Remarks  
 The window handle is a read-only value.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CStockPropImpl Class](../vs140/CStockPropImpl-Class.md)   
 [CStockPropImpl::get_Window](../vs140/CStockPropImpl--get_Window.md)