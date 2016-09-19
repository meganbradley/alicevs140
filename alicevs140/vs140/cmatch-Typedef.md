---
title: "cmatch Typedef"
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
ms.assetid: 9d41218e-28a1-4c5b-9bbb-fca1067fb1f5
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# cmatch Typedef
Type definition for char match_results.  
  
## Syntax  
  
```  
typedef match_results<const char*> cmatch;  
```  
  
## Remarks  
 The type describes a specialization of template class [match_results](../vs140/match_results-Class.md) for iterators of type `const char*`.  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [match_results](../vs140/match_results-Class.md)   
 [smatch](../vs140/smatch-Typedef.md)   
 [wcmatch](../vs140/wcmatch-Typedef.md)   
 [wsmatch](../vs140/wsmatch-Typedef.md)