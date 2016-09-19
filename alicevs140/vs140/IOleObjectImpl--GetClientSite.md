---
title: "IOleObjectImpl::GetClientSite"
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
ms.assetid: 9fede395-dfe7-48e2-a8d2-ff339626b705
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::GetClientSite
Puts the pointer in the control class data member [CComControlBase::m_spClientSite](../vs140/CComControlBase--m_spClientSite.md) into *ppClientSite* and increments the reference count on the pointer.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetClientSite)(  
   IOleClientSite** ppClientSite   
);  
```  
  
## Remarks  
 See [IOleObject::GetClientSite](http://msdn.microsoft.com/library/windows/desktop/ms692603) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::SetClientSite](../vs140/IOleObjectImpl--SetClientSite.md)