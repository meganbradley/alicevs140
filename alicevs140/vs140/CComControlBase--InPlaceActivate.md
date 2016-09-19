---
title: "CComControlBase::InPlaceActivate"
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
ms.assetid: acfd1f09-ef2c-40ba-a8fd-7270189d5d72
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::InPlaceActivate
Causes the control to transition from the inactive state to whatever state the verb in `iVerb` indicates.  
  
## Syntax  
  
```  
  
      HRESULT InPlaceActivate(  
   LONG iVerb,  
   const RECT* prcPosRect = NULL   
);  
```  
  
#### Parameters  
 `iVerb`  
 Value indicating the action to be performed by [IOleObjectImpl::DoVerb](../vs140/IOleObjectImpl--DoVerb.md).  
  
 *prcPosRect*  
 Pointer to the position of the in-place control.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Remarks  
 Before activation, this method checks that the control has a client site, checks how much of the control is visible, and gets the control's location in the parent window. After the control is activated, this method activates the control's user interface and tells the container to make the control visible.  
  
 This method also retrieves an `IOleInPlaceSite`, **IOleInPlaceSiteEx**, or **IOleInPlaceSiteWindowless** interface pointer for the control and stores it in the control class's data member [CComControlBase::m_spInPlaceSite](../vs140/CComControlBase--m_spInPlaceSite.md). The control class data members [CComControlBase::m_bInPlaceSiteEx](../vs140/CComControlBase--m_bInPlaceSiteEx.md), [CComControlBase::m_bWndLess](../vs140/CComControlBase--m_bWndLess.md), [CComControlBase::m_bWasOnceWindowless](../vs140/CComControlBase--m_bWasOnceWindowless.md), and [CComControlBase::m_bNegotiatedWnd](../vs140/CComControlBase--m_bNegotiatedWnd.md) are set to true as appropriate.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)