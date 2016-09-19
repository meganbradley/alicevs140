---
title: "CDacl::RemoveAllAces"
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
ms.assetid: c201d582-8d65-420b-a404-07ab6af9fa7c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDacl::RemoveAllAces
Removes all of the ACEs (access-control entries) contained in the `CDacl` object.  
  
## Syntax  
  
```  
  
void RemoveAllAces( ) throw( );  
  
```  
  
## Remarks  
 Removes every **ACE** (access-control entry) structure (if any) in the `CDacl` object.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CDacl Class](../vs140/CDacl-Class.md)   
 [CDacl::RemoveAce](../vs140/CDacl--RemoveAce.md)