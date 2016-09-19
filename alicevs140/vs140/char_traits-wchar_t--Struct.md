---
title: "char_traits&lt;wchar_t&gt; Struct"
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
ms.assetid: 31f34072-04d6-4871-88fe-48e17d473484
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# char_traits&lt;wchar_t&gt; Struct
A class that is a specialization of the template struct **char_traits<CharType\>** to an element of type `wchar_t`.  
  
## Syntax  
  
```  
template<> struct char_traits<wchar_t>;  
```  
  
## Remarks  
 Specialization allows the struct to take advantage of library functions that manipulate objects of this type `wchar_t`.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [char_traits Class](../vs140/char_traits-Struct.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)