---
title: "CRenderTarget::Flush"
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
ms.assetid: e4972623-776c-4a4c-bbc9-f06158fc7b83
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::Flush
Executes all pending drawing commands.  
  
## Syntax  
  
```  
void Flush(  
   D2D1_TAG* tag1 = NULL,  
   D2D1_TAG* tag2 = NULL  
);  
```  
  
#### Parameters  
 `tag1`  
 Contains the tag for drawing operations that caused errors or 0 if there were no errors. This parameter is passed uninitialized.  
  
 `tag2`  
 Contains the tag for drawing operations that caused errors or 0 if there were no errors. This parameter is passed uninitialized.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)