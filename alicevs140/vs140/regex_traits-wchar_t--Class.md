---
title: "regex_traits&lt;wchar_t&gt; Class"
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
ms.assetid: 288d6fdb-fb8e-4a4d-904a-53916be7f95b
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# regex_traits&lt;wchar_t&gt; Class
Specialization of regex_traits for wchar_t.  
  
## Syntax  
  
```  
template <>  
    class regex_traits<wchar_t>  
```  
  
## Remarks  
 The class is an explicit specialization of template class [regex_traits](../vs140/regex_traits-Class.md) for elements of type `wchar_t` (so that it can take advantage of library functions that manipulate objects of this type).  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [regex_traits](../vs140/regex_traits-Class.md)