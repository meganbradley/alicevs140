---
title: "wsregex_iterator Typedef"
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
ms.assetid: 34d06e96-f206-4f6f-a3cc-b7254f33484e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wsregex_iterator Typedef
Type definition for wstring regex_iterator.  
  
## Syntax  
  
```  
typedef regex_iterator<wstring::const_iterator> wsregex_iterator;  
```  
  
## Remarks  
 The type describes a specialization of template class [regex_iterator](../vs140/regex_iterator-Class.md) for iterators of type `wstring::const_iterator`.  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [regex_iterator](../vs140/regex_iterator-Class.md)   
 [cregex_iterator](../vs140/cregex_iterator-Typedef.md)   
 [sregex_iterator](../vs140/sregex_iterator-Typedef.md)   
 [wcregex_iterator](../vs140/wcregex_iterator-Typedef.md)