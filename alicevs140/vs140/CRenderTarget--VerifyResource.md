---
title: "CRenderTarget::VerifyResource"
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
ms.assetid: c0913772-6d11-47ee-b820-b173751e8259
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::VerifyResource
Verifies CD2DResource object validity; creates the object if it didn't already exist.  
  
## Syntax  
  
```  
BOOL VerifyResource(  
   CD2DResource* pResource  
);  
```  
  
#### Parameters  
 `pResource`  
 Pointer to CD2DResource object.  
  
## Return Value  
 TRUE is object if valid; otherwise FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)