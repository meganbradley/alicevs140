---
title: "CRenderTarget::FillRectangle"
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
ms.assetid: ee70d64d-e370-4c70-92c2-20e0f66b63ab
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::FillRectangle
Paints the interior of the specified rectangle.  
  
## Syntax  
  
```  
void FillRectangle(  
   const CD2DRectF& rect,  
   CD2DBrush* pBrush  
);  
```  
  
#### Parameters  
 `rect`  
 The dimension of the rectangle to paint, in device-independent pixels.  
  
 `pBrush`  
 The brush used to paint the rectangle's interior.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)