---
title: "basic_string::traits_type"
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
ms.assetid: f0161f16-f614-46ae-aeb2-5e5b2b2fd117
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_string::traits_type
A type for the character traits of the elements stored in a string.  
  
## Syntax  
  
```  
typedef Traits traits_type;  
```  
  
## Remarks  
 The type is a synonym for the second template parameter **Traits**.  
  
 For type **string**, it is equivalent to **char_traits<char\>**.  
  
## Example  
 See the example for [copy](../vs140/char_traits--copy.md) for an example of how to declare and use `traits_type`.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_string Class](../vs140/basic_string-Class.md)