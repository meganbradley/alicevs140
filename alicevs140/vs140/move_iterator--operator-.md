---
title: "move_iterator::operator-"
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
ms.assetid: 47ef168a-4a9d-4677-81b9-e503850cce31
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# move_iterator::operator-
Decrements the stored iterator and returns the indicated value.  
  
## Syntax  
  
```  
move_iterator operator-(difference_type _Off) const;  
```  
  
#### Parameters  
  
## Property Value/Return Value  
 Returns `move_iterator(*this) -= _Off`.  
  
## Remarks  
 The operator returns `move_iterator(*this) -= _Off`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [move_iterator Class](../vs140/move_iterator-Class.md)   
 [<iterator\>](../vs140/-iterator-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)