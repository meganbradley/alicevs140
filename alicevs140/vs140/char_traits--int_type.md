---
title: "char_traits::int_type"
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
ms.assetid: 7d709bb8-31f6-4033-8c35-7105d3c31f22
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# char_traits::int_type
An integer type that can represent a character of type `char_type` or an end-of-file (EOF) character.  
  
## Syntax  
  
```  
typedef long int_type;  
```  
  
## Remarks  
 It must be possible to type cast a value of type **CharType** to `int_type` then back to **CharType** without altering the original value.  
  
## Example  
 See the example for [eq_int_type](../vs140/char_traits--eq_int_type.md) for an example of how to declare and use `int_type`.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [char_traits Struct](../vs140/char_traits-Struct.md)