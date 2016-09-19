---
title: "CRenderTarget::GetTags"
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
ms.assetid: e173e057-30ea-4ef8-abaa-bbed151bc8de
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::GetTags
Gets the label for subsequent drawing operations.  
  
## Syntax  
  
```  
void GetTags(  
   D2D1_TAG *tag1 = NULL,  
   D2D1_TAG *tag2 = NULL  
) const;  
```  
  
#### Parameters  
 `tag1`  
 Contains the first label for subsequent drawing operations. This parameter is passed uninitialized. If NULL is specified, no value is retrieved for this parameter.  
  
 `tag2`  
 Contains the second label for subsequent drawing operations. This parameter is passed uninitialized. If NULL is specified, no value is retrieved for this parameter.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)