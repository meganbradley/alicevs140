---
title: "CDCRenderTarget::BindDC"
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
ms.assetid: f2674ee7-e0be-442a-a101-79dd2cd1b1c3
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDCRenderTarget::BindDC
Binds the render target to the device context to which it issues drawing commands  
  
## Syntax  
  
```  
BOOL BindDC(  
   const CDC& dc,  
   const CRect& rect  
);  
```  
  
#### Parameters  
 `dc`  
 The device context to which the render target issues drawing commands  
  
 `rect`  
 The dimensions of the handle to a device context (HDC) to which the render target is bound  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CDCRenderTarget Class](../vs140/CDCRenderTarget-Class.md)