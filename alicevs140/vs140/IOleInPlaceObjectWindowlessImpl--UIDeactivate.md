---
title: "IOleInPlaceObjectWindowlessImpl::UIDeactivate"
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
ms.assetid: 9f520596-681c-4d9d-b1b0-1e029d83ce26
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceObjectWindowlessImpl::UIDeactivate
Deactivates and removes the control's user interface that supports in-place activation.  
  
## Syntax  
  
```  
  
HRESULT UIDeactivate( );  
```  
  
## Remarks  
 Sets the control class's data member `m_bUIActive` to **FALSE**. The ATL implementation of this function always returns `S_OK`.  
  
 See [IOleInPlaceObject::UIDeactivate](http://msdn.microsoft.com/library/windows/desktop/ms693348) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceObjectWindowlessImpl Class](../vs140/IOleInPlaceObjectWindowlessImpl-Class.md)   
 [CComControlBase::m_bUIActive](../vs140/CComControlBase--m_bUIActive.md)