---
title: "CComPtrBase::Detach"
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
ms.assetid: 67c313ff-7903-42d2-81b3-ffc06878e29c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtrBase::Detach
Call this method to release ownership of a pointer.  
  
## Syntax  
  
```  
  
T* Detach( ) throw( );  
  
```  
  
## Return Value  
 Returns a copy of the pointer.  
  
## Remarks  
 Releases ownership of a pointer, sets the [CComPtrBase::p](../vs140/CComPtrBase--p.md) data member variable to NULL, and returns a copy of the pointer.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)   
 [CComPtrBase::Attach](../vs140/CComPtrBase--Attach.md)