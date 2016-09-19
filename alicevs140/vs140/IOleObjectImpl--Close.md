---
title: "IOleObjectImpl::Close"
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
ms.assetid: 0fe14103-925f-4472-886f-9796150ca4b5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::Close
Changes the control state from running to loaded.  
  
## Syntax  
  
```  
  
      STDMETHOD(Close)(  
   DWORD dwSaveOption   
);  
```  
  
## Remarks  
 Deactivates the control and destroys the control window if it exists. If the control class data member [CComControlBase::m_bRequiresSave](../vs140/CComControlBase--m_bRequiresSave.md) is **TRUE** and the `dwSaveOption` parameter is either `OLECLOSE_SAVEIFDIRTY` or `OLECLOSE_PROMPTSAVE`, the control properties are saved before closing.  
  
 The pointers held in the control class data members [CComControlBase::m_spInPlaceSite](../vs140/CComControlBase--m_spInPlaceSite.md) and [CComControlBase::m_spAdviseSink](../vs140/CComControlBase--m_spAdviseSink.md) are released, and the data members [CComControlBase::m_bNegotiatedWnd](../vs140/CComControlBase--m_bNegotiatedWnd.md), [CComControlBase::m_bWndless](../vs140/CComControlBase--m_bWndLess.md), and [CComControlBase::m_bInPlaceSiteEx](../vs140/CComControlBase--m_bInPlaceSiteEx.md) are set to **FALSE**.  
  
 See [IOleObject::Close](http://msdn.microsoft.com/library/windows/desktop/ms683922) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)