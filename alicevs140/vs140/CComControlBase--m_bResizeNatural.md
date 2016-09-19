---
title: "CComControlBase::m_bResizeNatural"
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
ms.assetid: b4ba8b98-d9bd-47f4-8925-69597861aee3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_bResizeNatural
Flag indicating the control wants to resize its natural extent (its unscaled physical size) when the container changes the control's display size.  
  
## Syntax  
  
```  
  
unsigned m_bResizeNatural:1;  
```  
  
## Remarks  
 This flag is checked by `IOleObjectImpl::SetExtent` and, if **TRUE**, the size passed into `SetExtent` is assigned to `m_sizeNatural`.  
  
 The size passed into `SetExtent` is always assigned to `m_sizeExtent`, regardless of the value of `m_bResizeNatural`.  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [IOleObjectImpl::SetExtent](../vs140/IOleObjectImpl--SetExtent.md)   
 [CComControlBase::m_sizeNatural](../vs140/CComControlBase--m_sizeNatural.md)   
 [CComControlBase::m_sizeExtent](../vs140/CComControlBase--m_sizeExtent.md)