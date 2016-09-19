---
title: "CRenderTarget::SetTransform"
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
ms.assetid: b0790d90-ff9b-42ff-8fc5-285c0056a4d0
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::SetTransform
Applies the specified transform to the render target, replacing the existing transformation. All subsequent drawing operations occur in the transformed space.  
  
## Syntax  
  
```  
void SetTransform(  
   const D2D1_MATRIX_3X2_F* transform  
);  
void SetTransform(  
   const D2D1_MATRIX_3X2_F& transform  
);  
```  
  
#### Parameters  
 `transform`  
 The transform to apply to the render target.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)