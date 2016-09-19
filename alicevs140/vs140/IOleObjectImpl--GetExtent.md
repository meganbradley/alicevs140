---
title: "IOleObjectImpl::GetExtent"
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
ms.assetid: fd207e1d-a8f1-4169-ae6d-b11591211bc4
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::GetExtent
Retrieves a running control's display size in HIMETRIC units (0.01 millimeter per unit).  
  
## Syntax  
  
```  
  
      STDMETHOD(GetExtent)(  
   DWORD dwDrawAspect,  
   SIZEL* psizel   
);  
```  
  
## Remarks  
 The size is stored in the control class data member [CComControlBase::m_sizeExtent](../vs140/CComControlBase--m_sizeExtent.md).  
  
 See [IOleObject::GetExtent](http://msdn.microsoft.com/library/windows/desktop/ms692325) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::SetExtent](../vs140/IOleObjectImpl--SetExtent.md)