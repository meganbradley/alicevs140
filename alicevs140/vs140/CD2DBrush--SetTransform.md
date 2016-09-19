---
title: "CD2DBrush::SetTransform"
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
ms.assetid: 10955722-0ca8-497a-9b79-0e058e12474b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DBrush::SetTransform
Applies the specified transform to the render target, replacing the existing transformation. All subsequent drawing operations occur in the transformed space  
  
## Syntax  
  
```  
void SetTransform(  
   const D2D1_MATRIX_3X2_F *transform  
);  
```  
  
#### Parameters  
 `transform`  
 The transform to apply to the render target  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DBrush Class](../vs140/CD2DBrush-Class.md)