---
title: "CComControlBase::m_bNegotiatedWnd"
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
ms.assetid: f7636340-8bed-459d-8465-990754e42800
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_bNegotiatedWnd
Flag indicating whether or not the control has negotiated with the container about support for OCX96 control features (such as flicker-free and windowless controls), and whether the control is windowed or windowless.  
  
## Syntax  
  
```  
  
unsigned m_bNegotiatedWnd:1;  
```  
  
## Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
 The `m_bNegotiatedWnd` flag must be **TRUE** for the `m_spInPlaceSite` pointer to be valid.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComControlBase::m_bWndLess](../vs140/CComControlBase--m_bWndLess.md)   
 [CComControlBase::m_spInPlaceSite](../vs140/CComControlBase--m_spInPlaceSite.md)