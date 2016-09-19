---
title: "CAcl::RemoveAces"
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
ms.topic: reference
ms.assetid: 3584ffbd-08b6-4dd1-9081-3093ff0de12e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAcl::RemoveAces
Removes alls ACEs (access-control entries) from the `CAcl` that apply to the given `CSid`.  
  
## Syntax  
  
```  
  
      bool RemoveAces(   
   const CSid & rSid   
) throw(...)  
```  
  
#### Parameters  
 `rSid`  
 A reference to a `CSid` object.  
  
## Returns  
 Returns true if successful, false if no ACEs are removed or the `CAcl` or `CSid` objects are invalid.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAcl Class](../vs140/CAcl-Class.md)   
 [CAcl::RemoveAce](../vs140/CAcl--RemoveAce.md)