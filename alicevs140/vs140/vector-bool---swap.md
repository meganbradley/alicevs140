---
title: "vector&lt;bool&gt;::swap"
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
ms.assetid: 5a2aa03c-63da-4327-9799-cb872cacad94
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector&lt;bool&gt;::swap
Static member function that exchanges two elements of Boolean vectors (`vector<bool>`) by using the proxy class [vector<bool\>::reference](../vs140/vector-bool---reference-Class.md).  
  
## Syntax  
  
```  
  
static void swap(  
    reference Left,  
    reference Right  
);  
```  
  
#### Parameters  
 `Left`  
 The element to be exchanged with the `Right` element.  
  
 `Right`  
 The element to be exchanged with the `Left` element.  
  
## Remarks  
 This overload supports the special proxy requirements of `vector<bool>`. [vector::swap](../vs140/vector--swap.md) has the same functionality as the single-argument overload of `vector<bool>::swap()`.  
  
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector Class](../vs140/vector-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)