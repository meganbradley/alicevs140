---
title: "move_iterator::operator-="
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
ms.assetid: 0311b2f2-74fa-4d94-809a-620a75bd67c4
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# move_iterator::operator-=
Moves across a specified number of previous elements. This operator subtracts an offset from the stored iterator.  
  
## Syntax  
  
```  
move_iterator& operator-=(  
    difference_type _Off  
);  
```  
  
#### Parameters  
  
## Property Value/Return Value  
 The operator returns `*this += -_Off.`  
  
## Remarks  
 The operator evaluates `*this += -_Off`. Then returns `*this`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [move_iterator Class](../vs140/move_iterator-Class.md)   
 [<iterator\>](../vs140/-iterator-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)