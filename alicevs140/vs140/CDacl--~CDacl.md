---
title: "CDacl::~CDacl"
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
ms.assetid: bde2f775-bc1e-44bc-847b-4dd10344911f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDacl::~CDacl
The destructor.  
  
## Syntax  
  
```  
  
~CDacl ( ) throw( );  
  
```  
  
## Remarks  
 The destructor frees any resources acquired by the object, including all ACEs (access-control entries) using [CDacl::RemoveAllAces](../vs140/CDacl--RemoveAllAces.md).  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CDacl Class](../vs140/CDacl-Class.md)   
 [CDacl::CDacl](../vs140/CDacl--CDacl.md)