---
title: "CComGITPtr::Detach"
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
ms.assetid: 37358422-88f1-4405-8cab-3ace8f10280b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComGITPtr::Detach
Call this method to disassociate the interface from the `CComGITPtr` object.  
  
## Syntax  
  
```  
  
DWORD Detach( ) throw( );  
  
```  
  
## Return Value  
 Returns the cookie from the `CComGITPtr` object.  
  
## Remarks  
 It is up to the caller to remove the interface from the GIT, using [CComGITPtr::Revoke](../vs140/CComGITPtr--Revoke.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComGITPtr Class](../vs140/CComGITPtr-Class.md)   
 [CComGITPtr::Attach](../vs140/CComGITPtr--Attach.md)