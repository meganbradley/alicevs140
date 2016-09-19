---
title: "CComPolyObject::FinalConstruct"
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
ms.assetid: 7b52ca37-ad80-4a2a-90c1-b5098226fdd4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPolyObject::FinalConstruct
Called during the final stages of object construction, this method performs any final initialization on the [m_contained](../vs140/CComPolyObject--m_contained.md) data member.  
  
## Syntax  
  
```  
  
HRESULT FinalConstruct( );  
  
```  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComPolyObject Class](../vs140/CComPolyObject-Class.md)   
 [CComObjectRootEx::FinalConstruct](../vs140/CComObjectRootEx--FinalConstruct.md)   
 [CComPolyObject::FinalRelease](../vs140/CComPolyObject--FinalRelease.md)