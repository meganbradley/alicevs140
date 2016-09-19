---
title: "CRenderTarget::RestoreDrawingState"
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
ms.assetid: fbbcd094-bf7c-403e-ba4a-98d7b6ead2c1
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::RestoreDrawingState
Sets the render target's drawing state to that of the specified ID2D1DrawingStateBlock.  
  
## Syntax  
  
```  
void RestoreDrawingState(  
   ID2D1DrawingStateBlock& drawingStateBlock  
);  
```  
  
#### Parameters  
 `drawingStateBlock`  
 The new drawing state of the render target.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)