---
title: "move_iterator::reference"
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
ms.assetid: fb5a5d3c-b001-4c54-bb1b-f16429a35c42
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# move_iterator::reference
The type `reference` is a `typedef` based on `value_type&&` for `move_iterator`, and can be used interchangeably with `value_type&&`.  
  
## Syntax  
  
```  
typedef value_type&&  
    reference;  
```  
  
## Remarks  
 The type is a synonym for `value_type&&`, which is an .  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [reference typedef](../vs140/move_iterator--reference.md)   
 [move_iterator Class](../vs140/move_iterator-Class.md)   
 [<iterator\>](../vs140/-iterator-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)