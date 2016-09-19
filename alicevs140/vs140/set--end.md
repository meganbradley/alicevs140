---
title: "set::end"
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
ms.assetid: 4625c297-803b-48e0-9f53-cb8ec9db5af8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::end
Returns the past-the-end iterator.  
  
## Syntax  
  
```  
const_iterator end( ) const;  
  
iterator end( );  
```  
  
## Return Value  
 The past-the-end iterator. If the set is empty, then `set::end() == set::begin()`.  
  
## Remarks  
 **end** is used to test whether an iterator has passed the end of its set.  
  
 The value returned by **end** should not be dereferenced.  
  
 For a code example, see [set::find](../vs140/set--find.md).  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)