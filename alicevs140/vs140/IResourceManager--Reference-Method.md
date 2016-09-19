---
title: "IResourceManager::Reference Method"
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
ms.topic: article
ms.assetid: 72cb0253-476a-4e0b-8999-2dfb4f384ee3
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IResourceManager::Reference Method
Increments the reference count on the Resource Manager instance.  
  
## Syntax  
  
```  
virtual unsigned int Reference() =0;  
```  
  
## Return Value  
 The resulting reference count.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IResourceManager Structure](../vs140/IResourceManager-Structure.md)   
 [IResourceManager::Release Method](../vs140/IResourceManager--Release-Method.md)