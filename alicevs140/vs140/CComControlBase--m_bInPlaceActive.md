---
title: "CComControlBase::m_bInPlaceActive"
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
ms.assetid: e3fc9e79-85e1-4864-9312-ecaf71f10304
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_bInPlaceActive
Flag indicating the control is in-place active.  
  
## Syntax  
  
```  
  
unsigned m_bInPlaceActive:1;  
```  
  
## Remarks  
 This means the control is visible and its window, if any, is visible, but its menus and toolbars may not be active. The `m_bUIActive` flag indicates the control's user interface, such as menus, is also active.  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComControlBase::m_bUIActive](../vs140/CComControlBase--m_bUIActive.md)