---
title: "CRenderTarget::GetTransform"
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
ms.assetid: 44b0b4bc-1246-45ba-ab5f-00bc21fbf532
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::GetTransform
Applies the specified transform to the render target, replacing the existing transformation. All subsequent drawing operations occur in the transformed space.  
  
## Syntax  
  
```  
void GetTransform(  
   D2D1_MATRIX_3X2_F* transform  
);  
```  
  
#### Parameters  
 `transform`  
 The transform to apply to the render target.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)