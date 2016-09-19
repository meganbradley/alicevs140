---
title: "move_iterator::operator"
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
ms.assetid: d1b9625b-f224-4fab-9d4e-ee45a772bae0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# move_iterator::operator
Allows array index access to elements across the range of the `move iterator`.  
  
## Syntax  
  
```  
reference operator[](difference_type _Off) const;  
```  
  
#### Parameters  
  
## Property Value/Return Value  
 Returns a reference to the value of the iterator at `_Off` offset.  
  
## Exceptions  
  
## Remarks  
 The operator returns `(reference)*(*this + _Off)`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [move_iterator Class](../vs140/move_iterator-Class.md)   
 [<iterator\>](../vs140/-iterator-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)