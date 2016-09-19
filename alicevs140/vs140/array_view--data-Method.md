---
title: "array_view::data Method"
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
ms.assetid: 5a834362-19e5-49be-88c0-25ddf978a2f4
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array_view::data Method
Returns a pointer to the raw data of the [array_view](../vs140/array_view-Class.md).  
  
## Syntax  
  
```  
_Value_type* data() const restrict(amp,cpu);  
  
const _Value_type* data() const restrict(amp,cpu);  
```  
  
## Return Value  
 A pointer to the raw data of the `array_view`.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array_view Class](../vs140/array_view-Class.md)