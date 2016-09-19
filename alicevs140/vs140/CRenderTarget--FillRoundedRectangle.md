---
title: "CRenderTarget::FillRoundedRectangle"
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
ms.assetid: 4037ae68-e4cd-4eb2-b19f-57f8aa1baeb6
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::FillRoundedRectangle
Paints the interior of the specified rounded rectangle.  
  
## Syntax  
  
```  
void FillRoundedRectangle(  
   const CD2DRoundedRect& rectRounded,  
   CD2DBrush* pBrush  
);  
```  
  
#### Parameters  
 `rectRounded`  
 The dimensions of the rounded rectangle to paint, in device independent pixels.  
  
 `pBrush`  
 The brush used to paint the interior of the rounded rectangle.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)