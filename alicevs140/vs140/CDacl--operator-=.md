---
title: "CDacl::operator ="
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
ms.assetid: 31c7c89d-d093-49f3-90e4-449261bc12ed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDacl::operator =
Assignment operator.  
  
## Syntax  
  
```  
  
      CDacl & operator =(  
   const ACL & rhs   
) throw(...);  
```  
  
#### Parameters  
 `rhs`  
 The ACL (access-control list) to assign to the existing object.  
  
## Return Value  
 Returns a reference to the updated `CDacl` object.  
  
## Remarks  
 You should ensure that you only pass a DACL (discretionary access-control list) to this function. Passing a SACL (system access-control list) to this function will cause an ASSERT in debug builds but will cause no error in release builds.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CDacl Class](../vs140/CDacl-Class.md)