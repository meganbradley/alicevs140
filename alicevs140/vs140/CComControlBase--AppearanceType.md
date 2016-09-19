---
title: "CComControlBase::AppearanceType"
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
ms.assetid: f841fd7f-383e-4658-a8f0-87f9d671ec21
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::AppearanceType
Override if your **m_nAppearance** stock property isn't of type **short**.  
  
## Syntax  
  
```  
  
typedef short AppearanceType;  
  
```  
  
## Remarks  
 The ATL Control Wizard adds **m_nAppearance** stock property of type short. Override `AppearanceType` if you use a different data type.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)