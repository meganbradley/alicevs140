---
title: "CRenderTarget::SaveDrawingState"
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
ms.assetid: 526e94f7-4e1e-480f-a152-fdd9fe06d948
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::SaveDrawingState
Saves the current drawing state to the specified ID2D1DrawingStateBlock.  
  
## Syntax  
  
```  
void SaveDrawingState(  
   ID2D1DrawingStateBlock& drawingStateBlock  
) const;  
```  
  
#### Parameters  
 `drawingStateBlock`  
 When this method returns, contains the current drawing state of the render target. This parameter must be initialized before passing it to the method.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)