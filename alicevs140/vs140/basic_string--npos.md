---
title: "basic_string::npos"
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
ms.assetid: 8c594660-1c76-4342-ab76-4dc0ef7fe0ff
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_string::npos
An unsigned integral value initialized to –1 that indicates either "not found" or "all remaining characters" when a search function fails.  
  
## Syntax  
  
```  
static const size_type npos = -1;  
```  
  
## Remarks  
 When the return value is to be checked for the `npos` value, it might not work unless the return value is of type [size_type](../vs140/basic_string--size_type.md) and not either `int` or `unsigned`.  
  
## Example  
 See the example for [find](../vs140/basic_string--find.md) for an example of how to declare and use `npos`.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_string Class](../vs140/basic_string-Class.md)