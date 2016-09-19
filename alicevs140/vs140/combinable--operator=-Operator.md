---
title: "combinable::operator= Operator"
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
ms.assetid: f7f22f4f-a028-4713-b638-dac4f5521a5c
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# combinable::operator= Operator
Assigns to a `combinable` object from another `combinable` object.  
  
## Syntax  
  
```  
combinable& operator=(  
   const combinable& _Copy  
);  
```  
  
#### Parameters  
 `_Copy`  
 An existing `combinable` object to be copied into this one.  
  
## Return Value  
 A reference to this `combinable` object.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [combinable Class](../vs140/combinable-Class.md)