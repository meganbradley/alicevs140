---
title: "IViewObjectExImpl::GetExtent"
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
ms.assetid: ff19fe02-b992-423e-9ab0-93c5cb5c2c81
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IViewObjectExImpl::GetExtent
Retrieves the control's display size in HIMETRIC units (0.01 millimeter per unit) from the control class data member [CComControlBase::m_sizeExtent](../vs140/CComControlBase--m_sizeExtent.md).  
  
## Syntax  
  
```  
  
      STDMETHOD(GetExtent)(  
   DWORD /* dwDrawAspect */,  
   LONG /* lindex */,  
   DVTARGETDEVICE* /* ptd */,  
   LPSIZEL* lpsizel   
);  
```  
  
## Remarks  
 See [IViewObject2::GetExtent](http://msdn.microsoft.com/library/windows/desktop/ms684032) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IViewObjectExImpl Class](../vs140/IViewObjectExImpl-Class.md)