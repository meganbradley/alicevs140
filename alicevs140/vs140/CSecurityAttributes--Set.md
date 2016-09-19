---
title: "CSecurityAttributes::Set"
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
ms.assetid: 1c908033-4ac3-46de-8f47-7da5f35f56ee
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityAttributes::Set
Call this method to set the attributes of the `CSecurityAttributes` object.  
  
## Syntax  
  
```  
  
      void Set(  
   const CSecurityDesc & rSecurityDescriptor,  
   bool bInheritHandle = false  
) throw(...);  
```  
  
#### Parameters  
 `rSecurityDescriptor`  
 Reference to a security descriptor.  
  
 `bInheritHandle`  
 Specifies whether the returned handle is inherited when a new process is created. If this member is true, the new process inherits the handle.  
  
## Remarks  
 This method is used by the constructor to initialize the `CSecurityAttributes` object.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityAttributes Class](../vs140/CSecurityAttributes-Class.md)