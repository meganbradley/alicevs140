---
title: "CComEnumImpl::m_spUnk"
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
ms.assetid: 6b2698a9-368c-4750-83e4-b63e49759db1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComEnumImpl::m_spUnk
This smart pointer maintains a reference on the object passed to [CComEnumImpl::Init](../vs140/CComEnumImpl--Init.md), ensuring that it remains alive during the lifetime of the enumerator.  
  
## Syntax  
  
```  
  
CComPtr<IUnknown> m_spUnk;  
  
```  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComEnumImpl Class](../vs140/CComEnumImpl-Class.md)   
 [CComEnumImpl::Init](../vs140/CComEnumImpl--Init.md)