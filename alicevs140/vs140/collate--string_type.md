---
title: "collate::string_type"
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
ms.assetid: 405af874-dbfd-4db7-9094-217c7f689663
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# collate::string_type
A type that describes a string of type `basic_string` containing characters of type **CharType**.  
  
## Syntax  
  
```  
  
typedef basic  
_  
string<CharType> string  
_  
type;  
  
```  
  
## Remarks  
 The type describes a specialization of template class [basic_string](../vs140/basic_string-Class.md) whose objects can store copies of the source sequence.  
  
## Example  
 For an example of how to declare and use `string_type`, see [transform](../vs140/collate--transform.md).  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [collate Class](../vs140/collate-Class.md)