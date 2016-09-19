---
title: "CComAggObject::FinalConstruct"
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
ms.assetid: 65e88e8e-3ae7-4060-89b6-b816d7888e49
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAggObject::FinalConstruct
Called during the final stages of object construction, this method performs any final initialization on the [m_contained](../vs140/CComAggObject--m_contained.md) member.  
  
## Syntax  
  
```  
  
HRESULT FinalConstruct( );  
  
```  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComAggObject Class](../vs140/CComAggObject-Class.md)   
 [CComObjectRootEx::FinalConstruct](../vs140/CComObjectRootEx--FinalConstruct.md)   
 [CComAggObject::FinalRelease](../vs140/CComAggObject--FinalRelease.md)