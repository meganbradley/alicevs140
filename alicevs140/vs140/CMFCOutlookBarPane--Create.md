---
title: "CMFCOutlookBarPane::Create"
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
ms.assetid: 1469b19b-e19d-4640-85fa-dedb372b2a3c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBarPane::Create
Creates the Outlook bar pane.  
  
## Syntax  
  
```  
virtual BOOL Create(  
   CWnd* pParentWnd,  
   DWORD dwStyle=AFX_DEFAULT_TOOLBAR_STYLE,  
   UINT uiID=(UINT)-1,  
   DWORD dwControlBarStyle=0   
);  
```  
  
#### Parameters  
 [in] `pParentWnd`  
 Specifies the parent window of the Outlook bar pane control. Must not be `NULL`.  
  
 [in] `dwStyle`  
 The window style.  For a list of window styles, see [Window Styles](../vs140/Window-Styles.md).  
  
 [in] `uiID`  
 The control ID. Must be unique to enable saving of the control's state.  
  
 [in] `dwControlBarStyle`  
 Specifies special styles that define the behavior of the Outlook bar pane control when it is detached from the Outlook bar.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise `FALSE`.  
  
## Remarks  
 To construct a `CMFCOutlookBarPane` object, first call the constructor, and then call `Create`, which creates the Outlook bar pane control and attaches it to the `CMFCOutlookBarPane` object.  
  
 For more information about `dwControlBarStyle` see [CBasePane::CreateEx](../vs140/CBasePane--CreateEx.md).  
  
## Requirements  
 **Header:** afxoutlookbarpane.h  
  
## See Also  
 [CMFCOutlookBarPane Class](../vs140/CMFCOutlookBarPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)