---
title: "IOleInPlaceObjectWindowlessImpl::GetWindow"
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
ms.assetid: a46c5606-707e-4af1-88af-a69c467f38fa
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleInPlaceObjectWindowlessImpl::GetWindow
The container calls this function to get the window handle of the control.  
  
## Syntax  
  
```  
  
      HRESULT GetWindow(  
   HWND* phwnd   
);  
```  
  
## Remarks  
 Some containers will not work with a control that has been windowless, even if it is currently windowed. In ATL's implementation, if the control class's data member `m_bWasOnceWindowless` is **TRUE**, the function returns **E_FAIL**. Otherwise, if *phwnd* is not **NULL**, `GetWindow` sets **phwnd* to the control class's data member `m_hWnd` and returns `S_OK`.  
  
 See [IOleWindow::GetWindow](http://msdn.microsoft.com/library/windows/desktop/ms687282) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleInPlaceObjectWindowlessImpl Class](../vs140/IOleInPlaceObjectWindowlessImpl-Class.md)   
 [CComControlBase::m_bWasOnceWindowless](../vs140/CComControlBase--m_bWasOnceWindowless.md)