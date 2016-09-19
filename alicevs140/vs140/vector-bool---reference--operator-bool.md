---
title: "vector&lt;bool&gt;::reference::operator bool"
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
ms.assetid: b0e57869-18cc-4296-9061-da502f30120d
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector&lt;bool&gt;::reference::operator bool
Provides an implicit conversion from `vector<bool>::reference` to `bool`.  
  
## Syntax  
  
```  
operator bool( ) const;  
```  
  
## Return Value  
 The Boolean value of the element of the [vector<bool\>](../vs140/vector-bool--Class.md) object.  
  
## Remarks  
 The `vector<bool>` object cannot be modified by this operator.  
  
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector<bool\>::reference Class](../vs140/vector-bool---reference-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)