---
title: "CComQIPtr::CComQIPtr"
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
ms.assetid: 3eb3f592-c246-479f-950a-9370f47a08f7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComQIPtr::CComQIPtr
The constructor.  
  
## Syntax  
  
```  
  
      CComQIPtr( ) throw( );   
CComQIPtr(  
   T* lp   
) throw( );  
CComQIPtr(  
   IUnknown* lp   
) throw( );  
CComQIPtr(  
   const CComQIPtr< T,  
   piid >& lp   
) throw( );  
```  
  
#### Parameters  
 `lp`  
 Used to initialize the interface pointer.  
  
 `T`  
 A COM interface.  
  
 `piid`  
 A pointer to the IID of `T`.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComQIPtr Class](../vs140/CComQIPtr-Class.md)