---
title: "CComGITPtr::Attach"
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
ms.assetid: fe5b8249-8919-409c-b9c7-1d2f799dfb0b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComGITPtr::Attach
Call this method to register the interface pointer in the global interface table (GIT).  
  
## Syntax  
  
```  
  
      HRESULT Attach(  
   T* p   
) throw( );  
HRESULT Attach(  
   DWORD dwCookie   
) throw( );  
```  
  
#### Parameters  
 `p`  
 The interface pointer to be added to the GIT.  
  
 `dwCookie`  
 The cookie used to identify the interface pointer.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 In debug builds, an assertion error will occur if the GIT is not valid, or if the cookie is equal to NULL.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComGITPtr Class](../vs140/CComGITPtr-Class.md)   
 [CComGITPtr::Detach](../vs140/CComGITPtr--Detach.md)