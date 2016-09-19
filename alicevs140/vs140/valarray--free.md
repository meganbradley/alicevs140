---
title: "valarray::free"
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
ms.assetid: 6c7f0551-f952-4ff0-8a52-3a7ec2de842c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# valarray::free
Frees the memory used by the valarray.  
  
## Syntax  
  
```  
void free();  
```  
  
## Remarks  
 This nonstandard function is equivalent to assigning an empty valarray. For example:  
  
```  
valarray<T> v;  
v = valarray<T>(); // equivalent to v.free()  
```  
  
## Requirements  
 **Header:** <valarray\>  
  
 **Namespace:** std  
  
## See Also  
 [valarray Class](../vs140/valarray-Class.md)