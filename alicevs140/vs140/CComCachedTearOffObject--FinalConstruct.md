---
title: "CComCachedTearOffObject::FinalConstruct"
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
ms.assetid: 5d5d0c3f-cde9-4f96-9fe0-03e952558bd8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCachedTearOffObject::FinalConstruct
Calls **m_contained::FinalConstruct** to create `m_contained`, the `CComContainedObject`<`contained`> object used to access the interface implemented by your tear-off class.  
  
## Syntax  
  
```  
  
HRESULT FinalConstruct( );  
```  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComCachedTearOffObject Class](../vs140/CComCachedTearOffObject-Class.md)   
 [CComCachedTearOffObject::FinalRelease](../vs140/CComCachedTearOffObject--FinalRelease.md)