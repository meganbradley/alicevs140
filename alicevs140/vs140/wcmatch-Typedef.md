---
title: "wcmatch Typedef"
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
ms.assetid: 69205378-2ab2-49e6-a6c4-b16d6b504ebe
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wcmatch Typedef
Type definition for wchar_t match_results.  
  
## Syntax  
  
```  
typedef match_results<const wchar_t *> wcmatch;  
```  
  
## Remarks  
 The type describes a specialization of template class [match_results](../vs140/match_results-Class.md) for iterators of type `const wchar_t*`.  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [match_results](../vs140/match_results-Class.md)   
 [cmatch](../vs140/cmatch-Typedef.md)   
 [smatch](../vs140/smatch-Typedef.md)   
 [wsmatch](../vs140/wsmatch-Typedef.md)