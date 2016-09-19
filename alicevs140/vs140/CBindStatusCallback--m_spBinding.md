---
title: "CBindStatusCallback::m_spBinding"
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
ms.assetid: fc3cb827-c93f-4e1c-abaf-e3763aa18e0d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::m_spBinding
A pointer to the `IBinding` interface of the current bind operation.  
  
## Syntax  
  
```  
  
CComPtr<IBinding> m_spBinding;  
  
```  
  
## Remarks  
 Initialized in `OnStartBinding` and released in `OnStopBinding`.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::OnStartBinding](../vs140/CBindStatusCallback--OnStartBinding.md)   
 [CBindStatusCallback::OnStopBinding](../vs140/CBindStatusCallback--OnStopBinding.md)   
 [CComPtr Class](../vs140/CComPtr-Class.md)