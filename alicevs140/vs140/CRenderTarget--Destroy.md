---
title: "CRenderTarget::Destroy"
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
ms.assetid: 13396c38-a432-48a3-9533-30f9d6c5ef67
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::Destroy
Deletes one or more resources  
  
## Syntax  
  
```  
BOOL Destroy(  
   BOOL bDeleteResources = TRUE  
);  
```  
  
#### Parameters  
 `bDeleteResources`  
 If bDeleteResources is TRUE, all resources located in m_lstResources will be automatically destroyed.  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)