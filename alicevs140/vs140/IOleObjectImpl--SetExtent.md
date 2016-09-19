---
title: "IOleObjectImpl::SetExtent"
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
ms.assetid: a68511b2-1f37-4dac-a86e-6e0a36a31cea
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::SetExtent
Sets the extent of the control's display area.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetExtent)(  
   DWORD dwDrawAspect,  
   SIZEL* psizel   
);  
```  
  
## Remarks  
 Otherwise, `SetExtent` stores the value pointed to by `psizel` in the control class data member [CComControlBase::m_sizeExtent](../vs140/CComControlBase--m_sizeExtent.md). This value is in HIMETRIC units (0.01 millimeter per unit).  
  
 If the control class data member [CComControlBase::m_bResizeNatural](../vs140/CComControlBase--m_bResizeNatural.md) is **TRUE**, `SetExtent` also stores the value pointed to by `psizel` in the control class data member [CComControlBase::m_sizeNatural](../vs140/CComControlBase--m_sizeNatural.md).  
  
 If the control class data member [CComControlBase::m_bRecomposeOnResize](../vs140/CComControlBase--m_bRecomposeOnResize.md) is **TRUE**, `SetExtent` calls `SendOnDataChange` and `SendOnViewChange` to notify all advisory sinks registered with the advise holder that the control size has changed.  
  
 See [IOleObject::SetExtent](http://msdn.microsoft.com/library/windows/desktop/ms694330) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::GetExtent](../vs140/IOleObjectImpl--GetExtent.md)   
 [CComControlBase::SendOnDataChange](../vs140/CComControlBase--SendOnDataChange.md)   
 [CComControlBase::SendOnViewChange](../vs140/CComControlBase--SendOnViewChange.md)