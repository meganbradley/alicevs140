---
title: "CD2DBitmap::CopyFromRenderTarget"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: f89c81e2-de79-403f-80af-d1cad568978d
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DBitmap::CopyFromRenderTarget
Copies the specified region from the specified render target into the current bitmap  
  
## Syntax  
  
```  
HRESULT CopyFromRenderTarget(  
   const CRenderTarget* pRenderTarget,  
   const CD2DPointU* destPoint = NULL,  
   const CD2DRectU* srcRect = NULL  
);  
```  
  
#### Parameters  
 `pRenderTarget`  
 The render target that contains the region to copy  
  
 `destPoint`  
 In the current bitmap, the upper-left corner of the area to which the region specified by srcRect is copied  
  
 `srcRect`  
 The area of renderTarget to copy  
  
## Return Value  
 If the method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DBitmap Class](../vs140/CD2DBitmap-Class.md)