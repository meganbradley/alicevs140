---
title: "extent::operator= Operator"
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
ms.assetid: b0c8f537-3606-4781-8788-3b0d08cbd62e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# extent::operator= Operator
Copies the contents of another [extent](../vs140/extent-Class--C---AMP-.md) object into this one.  
  
## Syntax  
  
```  
extent<_Rank>& operator=(  
   const extent<_Rank>& _Other  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Other`  
 The `extent` object to copy from.  
  
## Return Value  
 A reference to this `extent` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [extent Structure](../vs140/extent-Class--C---AMP-.md)