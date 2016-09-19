---
title: "CD2DLinearGradientBrush::Create"
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
ms.assetid: 76acd41e-adba-429c-83b0-3cb3afd9fe3c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DLinearGradientBrush::Create
Creates a CD2DLinearGradientBrush.  
  
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
 [CD2DLinearGradientBrush Class](../vs140/CD2DLinearGradientBrush-Class.md)