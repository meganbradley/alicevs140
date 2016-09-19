---
title: "wsmatch Typedef"
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
ms.assetid: 834ec92d-e1f9-49c5-b731-b387ec04c3bb
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wsmatch Typedef
Type definition for wstring match_results.  
  
## Syntax  
  
```  
typedef match_results<wstring::const_iterator> wsmatch;  
```  
  
## Remarks  
 The type describes a specialization of template class [match_results](../vs140/match_results-Class.md) for iterators of type `wstring::const_iterator`.  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [match_results](../vs140/match_results-Class.md)   
 [cmatch](../vs140/cmatch-Typedef.md)   
 [smatch](../vs140/smatch-Typedef.md)   
 [wcmatch](../vs140/wcmatch-Typedef.md)