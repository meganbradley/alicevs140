---
title: "CComControlBase::GetDirty"
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
ms.assetid: c51ad3f3-d10f-49cc-829e-506af6a47108
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetDirty
Returns the value of data member `m_bRequiresSave`.  
  
## Syntax  
  
```  
  
BOOL GetDirty( );  
  
```  
  
## Return Value  
 Returns the value of data member [m_bRequiresSave](../vs140/CComControlBase--m_bRequiresSave.md).  
  
## Remarks  
 This value is set using [CComControlBase::SetDirty](../vs140/CComControlBase--SetDirty.md).  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)