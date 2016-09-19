---
title: "CComPtr::CComPtr"
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
ms.assetid: 33f47c89-4a34-4647-92cc-2137915cf5dd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtr::CComPtr
The constructor.  
  
## Syntax  
  
```  
  
      CComPtr( ) throw ( );   
CComPtr(  
   T* lp   
) throw ( );  
CComPtr (  
   const CComPtr< T >& lp   
) throw ( );  
```  
  
#### Parameters  
 `lp`  
 Used to initialize the interface pointer.  
  
 `T`  
 A COM interface.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtr Class](../vs140/CComPtr-Class.md)