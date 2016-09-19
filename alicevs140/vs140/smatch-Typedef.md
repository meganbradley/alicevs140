---
title: "smatch Typedef"
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
ms.assetid: 95012f1a-d9bc-4cd5-b846-99c04e8e869a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# smatch Typedef
Type definition for string match_results.  
  
## Syntax  
  
```  
typedef match_results<string::const_iterator> smatch;  
```  
  
## Remarks  
 The type describes a specialization of template class [match_results](../vs140/match_results-Class.md) for iterators of type `string::const_iterator`.  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [match_results](../vs140/match_results-Class.md)   
 [cmatch](../vs140/cmatch-Typedef.md)   
 [wcmatch](../vs140/wcmatch-Typedef.md)   
 [wsmatch](../vs140/wsmatch-Typedef.md)