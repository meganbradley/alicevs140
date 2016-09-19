---
title: "IEnumOnSTLImpl::m_spUnk"
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
ms.assetid: 680fe80b-1b06-4cb0-8b99-08525486082a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IEnumOnSTLImpl::m_spUnk
The **IUnknown** pointer of the object supplying the collection.  
  
## Syntax  
  
```  
  
CComPtr<IUnknown> m_spUnk;  
  
```  
  
## Remarks  
 This smart pointer maintains a reference on the object passed to [IEnumOnSTLImpl::Init](../vs140/IEnumOnSTLImpl--Init.md), ensuring that it remains alive during the lifetime of the enumerator.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IEnumOnSTLImpl Class](../vs140/IEnumOnSTLImpl-Class.md)   
 [IEnumOnSTLImpl::Init](../vs140/IEnumOnSTLImpl--Init.md)