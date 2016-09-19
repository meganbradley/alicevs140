---
title: "CD2DBrush::GetTransform"
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
ms.assetid: 4b8cf14f-b3a7-4900-9c8f-952fdcf42371
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DBrush::GetTransform
Gets the current transform of the render target  
  
## Syntax  
  
```  
void GetTransform(  
   D2D1_MATRIX_3X2_F *transform  
) const;  
```  
  
#### Parameters  
 `transform`  
 When this returns, contains the current transform of the render target. This parameter is passed uninitialized  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DBrush Class](../vs140/CD2DBrush-Class.md)