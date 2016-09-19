---
title: "CHwndRenderTarget::Resize"
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
ms.assetid: 66ff9633-6df7-47c0-8403-413513d907bd
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHwndRenderTarget::Resize
Changes the size of the render target to the specified pixel size  
  
## Syntax  
  
```  
BOOL Resize(  
   const CD2DSizeU& size  
);  
```  
  
#### Parameters  
 `size`  
 The new size of the render target in device pixels  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CHwndRenderTarget Class](../vs140/CHwndRenderTarget-Class.md)