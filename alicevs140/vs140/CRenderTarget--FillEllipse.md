---
title: "CRenderTarget::FillEllipse"
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
ms.assetid: 7d0dcf2f-815e-4863-bf8d-179e2f78681b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::FillEllipse
Paints the interior of the specified ellipse.  
  
## Syntax  
  
```  
void FillEllipse(  
   const CD2DEllipse& ellipse,  
   CD2DBrush* pBrush  
);  
```  
  
#### Parameters  
 `ellipse`  
 The position and radius, in device-independent pixels, of the ellipse to paint.  
  
 `pBrush`  
 The brush used to paint the interior of the ellipse.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)