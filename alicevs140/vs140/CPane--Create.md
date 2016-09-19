---
title: "CPane::Create"
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
ms.assetid: ace97db5-cc11-4300-98f8-68d0c7e10797
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::Create
Creates a control bar and attaches it to the [CPane](../vs140/CPane-Class.md) object.  
  
## Syntax  
  
```  
virtual BOOL Create(  
    LPCTSTR lpszClassName,  
    DWORD dwStyle,  
    const RECT& rect,  
    CWnd* pParentWnd,  
    UINT nID,  
    DWORD dwControlBarStyle = AFX_DEFAULT_PANE_STYLE,  
    CCreateContext* pContext = NULL  
);  
```  
  
#### Parameters  
 [in] `lpszClassName`  
 Specifies the name of the Windows class.  
  
 [in] `dwStyle`  
 Specifies the window style attributes. For more information, see [Window Styles](../vs140/Window-Styles.md).  
  
 [in] `rect`  
 Specifies the initial size and position of the `pParentWnd` window, in client coordinates.  
  
 [in] [out] `pParentWnd`  
 Specifies the parent window of this pane.  
  
 [in] `nID`  
 Specifies the ID of the pane.  
  
 [in] `dwControlBarStyle`  
 Specifies the style for the pane. For more information, see [CBasePane::CreateEx](../vs140/CBasePane--CreateEx.md).  
  
 [in] [out] `pContext`  
 Specifies the create context of the pane.  
  
## Return Value  
 `TRUE` if the pane was created successfully; otherwise, `FALSE`.  
  
## Remarks  
 This method creates a Windows pane and attaches it to the `CPane` object.  
  
 If you have not explicitly initialized [CPane::m_recentDockInfo](../vs140/CPane--m_recentDockInfo.md) before you call `Create`, the parameter `rect` will be used as the rectangle when floating or docking the pane.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecentDockSiteInfo Class](../vs140/CRecentDockSiteInfo-Class.md)   
 [CBasePane::CreateEx](../vs140/CBasePane--CreateEx.md)