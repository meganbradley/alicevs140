---
title: "tuple:swap"
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
ms.assetid: 4b4386d8-2a04-47a9-aaf7-8185d40b2623
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# tuple:swap
Exchanges the elements of two tuples.  
  
## Syntax  
  
```  
template<class... Types>  
    void swap(tuple<Types...&> left,  
        tuple<Types...&> right);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`left`|A tuple whose elements are to be exchanged with those of the tuple `right`.|  
|`right`|A tuple whose elements are to be exchanged with those of the tuple `left`.|  
  
## Remarks  
 The function executes `left.swap(right)`.  
  
## Requirements  
 **Header:** <tuple\>  
  
 **Namespace:** std  
  
## See Also  
 [<tuple\>](../vs140/-tuple-.md)   
 [tuple Class](../vs140/tuple-Class.md)