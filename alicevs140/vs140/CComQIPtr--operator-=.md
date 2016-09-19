---
title: "CComQIPtr::operator ="
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
ms.assetid: 11e1a23e-c013-4e76-805e-d9daaa345f07
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComQIPtr::operator =
The assignment operator.  
  
## Syntax  
  
```  
  
      T  
      * operator =(  
   T* lp   
) throw( );  
T* operator =(  
   const CComQIPtr< T,  
   piid >& lp   
) throw( );  
T* operator =(  
   IUnknown* lp   
) throw( );  
```  
  
#### Parameters  
 `lp`  
 Used to initialize the interface pointer.  
  
 `T`  
 A COM interface.  
  
 `piid`  
 A pointer to the IID of `T`.  
  
## Return Value  
 Returns a pointer to the updated `CComQIPtr` object.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComQIPtr Class](../vs140/CComQIPtr-Class.md)   
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)