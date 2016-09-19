---
title: "CRenderTarget::GetTextRenderingParams"
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
ms.assetid: b84bc7a8-5d9c-40cc-9154-8ef036f2d583
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::GetTextRenderingParams
Retrieves the render target's current text rendering options.  
  
## Syntax  
  
```  
void GetTextRenderingParams(  
   IDWriteRenderingParams** textRenderingParams  
);  
```  
  
#### Parameters  
 `textRenderingParams`  
 When this method returns, textRenderingParamscontains the address of a pointer to the render target's current text rendering options.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)