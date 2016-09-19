---
title: "array_view::refresh Method"
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
ms.assetid: 8b029f8e-a7a7-40c6-83a7-ef8c9e5df0cd
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array_view::refresh Method
Notifies the [array_view](../vs140/array_view-Class.md) object that its bound memory has been modified outside the `array_view` interface. A call to this method renders all cached information stale.  
  
## Syntax  
  
```  
void refresh() const restrict(cpu);  
```  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array_view Class](../vs140/array_view-Class.md)