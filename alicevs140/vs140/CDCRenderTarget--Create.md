---
title: "CDCRenderTarget::Create"
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
ms.assetid: 75acdc0c-cc7a-4579-b04a-de63383ccac2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDCRenderTarget::Create
Creates a CDCRenderTarget.  
  
## Syntax  
  
```  
BOOL Create(  
   const D2D1_RENDER_TARGET_PROPERTIES& props  
);  
```  
  
#### Parameters  
 `props`  
 The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering.  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CDCRenderTarget Class](../vs140/CDCRenderTarget-Class.md)