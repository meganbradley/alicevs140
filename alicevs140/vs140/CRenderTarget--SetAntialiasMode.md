---
title: "CRenderTarget::SetAntialiasMode"
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
ms.assetid: 19113d08-4bcb-4966-97fa-b560a253beaf
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::SetAntialiasMode
Sets the antialiasing mode of the render target. The antialiasing mode applies to all subsequent drawing operations, excluding text and glyph drawing operations.  
  
## Syntax  
  
```  
void SetAntialiasMode(  
   D2D1_ANTIALIAS_MODE antialiasMode  
);  
```  
  
#### Parameters  
 `antialiasMode`  
 The antialiasing mode for future drawing operations.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)