---
title: "CSacl::RemoveAllAces"
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
ms.assetid: 0e5df22f-424b-4191-91f5-c45eceb1b55b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSacl::RemoveAllAces
Removes all of the access-control entries (ACEs) contained in the `CSacl` object.  
  
## Syntax  
  
```  
  
void RemoveAllAces( ) throw( );  
  
```  
  
## Remarks  
 Removes every **ACE** structure (if any) in the `CSacl` object.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSacl Class](../vs140/CSacl-Class.md)   
 [CSacl::RemoveAce](../vs140/CSacl--RemoveAce.md)