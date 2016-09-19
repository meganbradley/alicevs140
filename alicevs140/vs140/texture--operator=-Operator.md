---
title: "texture::operator= Operator"
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
ms.assetid: 9173a95c-15d7-4aae-a115-8cd51ec59b0f
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# texture::operator= Operator
Copies the specified [texture](../vs140/texture-Class.md) object to this one.  
  
## Syntax  
  
```  
texture& operator=(  
   const texture & _Other  
);  
  
texture& operator=(  
   texture<_Value_type, _Rank> && _Other  
);  
```  
  
#### Parameters  
 `_Other`  
 The [texture](../vs140/texture-Class.md) object to copy from.  
  
## Return Value  
 A reference to this [texture](../vs140/texture-Class.md) object.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency::graphics  
  
## See Also  
 [texture Class](../vs140/texture-Class.md)