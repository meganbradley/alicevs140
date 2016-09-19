---
title: "index::operator= Operator"
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
ms.assetid: 26b659c5-a288-4045-8185-3204ed05e830
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# index::operator= Operator
Copies the contents of the specified [index](../vs140/index-Class.md) object into this one.  
  
## Syntax  
  
```  
index<_Rank>& operator=(  
   const index<_Rank>& _Other  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Other`  
 The `index` object to copy from.  
  
## Return Value  
 A reference to this `index` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [index Structure](../vs140/index-Class.md)