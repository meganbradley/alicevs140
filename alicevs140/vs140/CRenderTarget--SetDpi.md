---
title: "CRenderTarget::SetDpi"
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
ms.assetid: 082b99ba-b518-4663-b0dd-2dee7f47feaf
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::SetDpi
Sets the dots per inch (DPI) of the render target.  
  
## Syntax  
  
```  
void SetDpi(  
   const CD2DSizeF& sizeDPI  
);  
```  
  
#### Parameters  
 `sizeDPI`  
 A value greater than or equal to zero that specifies the horizontal/verticalDPI of the render target.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)