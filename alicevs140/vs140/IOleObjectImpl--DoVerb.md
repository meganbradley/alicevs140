---
title: "IOleObjectImpl::DoVerb"
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
ms.assetid: 9176fbda-13c1-485d-8d10-fc3475b56e2a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::DoVerb
Tells the control to perform one of its enumerated actions.  
  
## Syntax  
  
```  
  
      STDMETHOD(DoVerb)(  
   LONG iVerb,  
   LPMSG /* pMsg */,  
   IOleClientSite* pActiveSite,  
   LONG /* lindex */,  
   HWND hwndParent,  
   LPCRECT lprcPosRect   
);  
```  
  
## Remarks  
 Depending on the value of `iVerb`, one of the ATL `DoVerb` helper functions is called as follows:  
  
|*iVerb* Value|DoVerb helper function called|  
|-------------------|-----------------------------------|  
|**OLEIVERB_DISCARDUNDOSTATE**|[DoVerbDiscardUndo](../vs140/IOleObjectImpl--DoVerbDiscardUndo.md)|  
|`OLEIVERB_HIDE`|[DoVerbHide](../vs140/IOleObjectImpl--DoVerbHide.md)|  
|**OLEIVERB_INPLACEACTIVATE**|[DoVerbInPlaceActivate](../vs140/IOleObjectImpl--DoVerbInPlaceActivate.md)|  
|`OLEIVERB_OPEN`|[DoVerbOpen](../vs140/IOleObjectImpl--DoVerbOpen.md)|  
|`OLEIVERB_PRIMARY`|[DoVerbPrimary](../vs140/IOleObjectImpl--DoVerbPrimary.md)|  
|**OLEIVERB_PROPERTIES**|[CComControlBase::DoVerbProperties](../vs140/CComControlBase--DoVerbProperties.md)|  
|`OLEIVERB_SHOW`|[DoVerbShow](../vs140/IOleObjectImpl--DoVerbShow.md)|  
|`OLEIVERB_UIACTIVATE`|[DoVerbUIActivate](../vs140/IOleObjectImpl--DoVerbUIActivate.md)|  
  
 See [IOleObject::DoVerb](http://msdn.microsoft.com/library/windows/desktop/ms694508) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObject::EnumVerbs](http://msdn.microsoft.com/library/windows/desktop/ms692781)