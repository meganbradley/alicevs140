---
title: "wcregex_iterator Typedef"
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
ms.assetid: 90103d1a-71ae-4a37-8236-8231b5a05f9b
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# wcregex_iterator Typedef
Type definition for wchar_t regex_iterator.  
  
## Syntax  
  
```  
typedef regex_iterator<const wchar_t*> wcregex_iterator;  
```  
  
## Remarks  
 The type describes a specialization of template class [regex_iterator](../vs140/regex_iterator-Class.md) for iterators of type `const wchar_t*`.  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [regex_iterator](../vs140/regex_iterator-Class.md)   
 [cregex_iterator](../vs140/cregex_iterator-Typedef.md)   
 [sregex_iterator](../vs140/sregex_iterator-Typedef.md)   
 [wsregex_iterator](../vs140/wsregex_iterator-Typedef.md)