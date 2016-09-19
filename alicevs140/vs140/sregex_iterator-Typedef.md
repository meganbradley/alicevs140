---
title: "sregex_iterator Typedef"
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
ms.assetid: 9683b0d2-5cd3-4219-8ed3-3234617738ec
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# sregex_iterator Typedef
Type definition for string regex_iterator.  
  
## Syntax  
  
```  
typedef regex_iterator<string::const_iterator> sregex_iterator;  
```  
  
## Remarks  
 The type describes a specialization of template class [regex_iterator](../vs140/regex_iterator-Class.md) for iterators of type `string::const_iterator`.  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [regex_iterator](../vs140/regex_iterator-Class.md)   
 [cregex_iterator](../vs140/cregex_iterator-Typedef.md)   
 [wcregex_iterator](../vs140/wcregex_iterator-Typedef.md)   
 [wsregex_iterator](../vs140/wsregex_iterator-Typedef.md)