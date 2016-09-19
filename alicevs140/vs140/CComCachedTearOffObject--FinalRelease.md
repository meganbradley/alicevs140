---
title: "CComCachedTearOffObject::FinalRelease"
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
ms.assetid: 7ed286b0-18cf-4e1a-aab0-c2f6da366ae4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCachedTearOffObject::FinalRelease
Calls **m_contained::FinalRelease** to free `m_contained`, the `CComContainedObject`<`contained`> object.  
  
## Syntax  
  
```  
  
void FinalRelease( );  
```  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComCachedTearOffObject Class](../vs140/CComCachedTearOffObject-Class.md)   
 [CComCachedTearOffObject::FinalConstruct](../vs140/CComCachedTearOffObject--FinalConstruct.md)