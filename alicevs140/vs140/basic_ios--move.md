---
title: "basic_ios::move"
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
ms.assetid: 1f622771-3877-477f-852b-1b77dd1cd754
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ios::move
Moves all values, except the pointer to the stream buffer, from the parameter to the current object.  
  
## Syntax  
  
```  
void move(  
   basic_ios&& _Right  
);  
```  
  
#### Parameters  
 `_Right`  
 The `ios_base` object to move values from.  
  
## Property Value/Return Value  
  
## Exceptions  
  
## Remarks  
 The protected member function moves all the values stored in `_Right` to `*this` except the stored `stream buffer pointer`, which is unchanged in `_Right` and set to a null pointer in `*this`. The stored `tie pointer` is set to a null pointer in `_Right`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)