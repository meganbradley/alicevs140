---
title: "CComAggObject::FinalRelease"
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
ms.assetid: 191a9fe8-f233-4c31-9325-ebe0646be213
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAggObject::FinalRelease
Called during object destruction, this method frees the [m_contained](../vs140/CComAggObject--m_contained.md) member.  
  
## Syntax  
  
```  
  
void FinalRelease( );  
  
```  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComAggObject Class](../vs140/CComAggObject-Class.md)   
 [CComObjectRootEx::FinalRelease](../vs140/CComObjectRootEx--FinalRelease.md)   
 [CComAggObject::FinalConstruct](../vs140/CComAggObject--FinalConstruct.md)