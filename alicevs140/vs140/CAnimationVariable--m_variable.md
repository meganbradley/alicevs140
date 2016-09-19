---
title: "CAnimationVariable::m_variable"
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
ms.assetid: 0083cb64-09db-4b75-bea1-ff66179af2a7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationVariable::m_variable
Stores a pointer to IUIAnimationVariable COM object. NULL if the COM object has not been created yet, or if creation failed.  
  
## Syntax  
  
```  
ATL::CComPtr<IUIAnimationVariable> m_variable;  
```  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationVariable Class](../vs140/CAnimationVariable-Class.md)