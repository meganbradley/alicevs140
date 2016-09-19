---
title: "basic_string::reference"
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
ms.assetid: 90a29a1c-7d19-45bf-bd43-db28141b40de
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_string::reference
A type that provides a reference to an element stored in a string.  
  
## Syntax  
  
```  
typedef typename allocator_type::reference reference;  
```  
  
## Remarks  
 A type **reference** can be used to modify the value of an element.  
  
 The type is a synonym for **allocator_type::reference**.  
  
 For type **string**, it is equivalent to **chr&**.  
  
## Example  
 See the example for [at](../vs140/basic_string--at.md) for an example of how to declare and use **reference**.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_string Class](../vs140/basic_string-Class.md)