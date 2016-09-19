---
title: "CAcl::CAceTypeArray"
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
ms.assetid: 1337c7b8-b78b-4e46-8337-beb0aee950f8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAcl::CAceTypeArray
An array of BYTEs.  
  
## Syntax  
  
```  
  
typedef CAtlArray<BYTE> CAceTypeArray;  
  
```  
  
## Remarks  
 This typedef specifies the array type used to define the nature of the access-control entry (ACE) objects, such as ACCESS_ALLOWED_ACE_TYPE or ACCESS_DENIED_ACE_TYPE. See the [ACE_HEADER](http://msdn.microsoft.com/library/windows/desktop/aa374919) definition for the complete list of possible types.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAcl Class](../vs140/CAcl-Class.md)   
 [ACE_HEADER](http://msdn.microsoft.com/library/windows/desktop/aa374919)