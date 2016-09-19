---
title: "CD2DRadialGradientBrush::Create"
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
ms.assetid: 203a8b78-7bb9-4291-b22e-cc8c2d9ebee7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DRadialGradientBrush::Create
Creates a CD2DRadialGradientBrush.  
  
## Syntax  
  
```  
virtual HRESULT Create(  
   CRenderTarget* pRenderTarget  
);  
```  
  
#### Parameters  
 `pRenderTarget`  
 A pointer to the render target.  
  
## Return Value  
 If the method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DRadialGradientBrush Class](../vs140/CD2DRadialGradientBrush-Class.md)