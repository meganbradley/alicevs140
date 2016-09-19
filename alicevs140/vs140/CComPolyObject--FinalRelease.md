---
title: "CComPolyObject::FinalRelease"
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
ms.assetid: 14618d7e-895c-4229-ad77-e8c73f00bed1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPolyObject::FinalRelease
Called during object destruction, this method frees the [m_contained](../vs140/CComPolyObject--m_contained.md) data member.  
  
## Syntax  
  
```  
  
void FinalRelease( );  
  
```  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComPolyObject Class](../vs140/CComPolyObject-Class.md)   
 [CComObjectRootEx::FinalRelease](../vs140/CComObjectRootEx--FinalRelease.md)   
 [CComPolyObject::FinalConstruct](../vs140/CComPolyObject--FinalConstruct.md)