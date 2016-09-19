---
title: "regex Typedef"
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
ms.assetid: 0462858e-f011-4b04-9ac4-86b4de624064
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# regex Typedef
Type definition for char basic_regex.  
  
## Syntax  
  
```  
typedef basic_regex<char> regex;  
```  
  
## Remarks  
 The type describes a specialization of template class [basic_regex](../vs140/basic_regex-Class.md) for elements of type `char`.  
  
> [!NOTE]
>  High-bit characters will have unpredictable results with `regex`. Values outside the range of 0 to 127 may result in undefined behavior.  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [wregex](../vs140/wregex-Typedef.md)