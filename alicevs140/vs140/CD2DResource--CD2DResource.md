---
title: "CD2DResource::CD2DResource"
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
ms.assetid: 2fc94565-328b-44da-a901-8b077d1ae234
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DResource::CD2DResource
Constructs a CD2DResource object.  
  
## Syntax  
  
```  
CD2DResource(  
   CRenderTarget* pParentTarget,  
   BOOL bAutoDestroy  
);  
```  
  
#### Parameters  
 `pParentTarget`  
 A pointer to the render target.  
  
 `bAutoDestroy`  
 Indicates that the object will be destroyed by owner (pParentTarget).  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DResource Class](../vs140/CD2DResource-Class.md)