---
title: "texture::data Method"
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
ms.assetid: dda01f88-a19a-4161-85cc-3b197b095187
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# texture::data Method
Returns a CPU pointer to the raw data of this texture.  
  
## Syntax  
  
```  
void* data() restrict(cpu);  
  
const void* data() const restrict(cpu);  
```  
  
## Return Value  
 A pointer to the raw data of the texture.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** concurrency::graphics  
  
## See Also  
 [texture Class](../vs140/texture-Class.md)