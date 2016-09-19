---
title: "CToolTipCtrl::Create"
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
ms.assetid: f0ff5ace-e71a-479b-803c-0267db771a4d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::Create
Creates a tool tip control and attaches it to a `CToolTipCtrl` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   CWnd* pParentWnd,  
   DWORD dwStyle = 0   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 Specifies the tool tip control's parent window, usually a `CDialog`. It must not be **NULL**.  
  
 `dwStyle`  
 Specifies the tool tip control's style. See the **Remarks** section for more information.  
  
## Return Value  
 Nonzero if the `CToolTipCtrl` object is successfully created; otherwise 0.  
  
## Remarks  
 You construct a `CToolTipCtrl` in two steps. First, call the constructor to construct the `CToolTipCtrl` object, and then call **Create** to create the tool tip control and attach it to the `CToolTipCtrl` object.  
  
 The `dwStyle` parameter can be any combination of [Window Styles](../vs140/Window-Styles.md). In addition, a tool tip control has two class-specific styles: **TTS_ALWAYSTIP** and **TTS_NOPREFIX**.  
  
|Style|Meaning|  
|-----------|-------------|  
|**TTS_ALWAYSTIP**|Specifies that the tool tip will appear when the cursor is on a tool, regardless of whether the tool tip control's owner window is active or inactive. Without this style, the tool tip control appears when the tool's owner window is active, but not when it is inactive.|  
|**TTS_NOPREFIX**|This style prevents the system from stripping the ampersand (&) character from a string. If a tool tip control does not have the **TTS_NOPREFIX** style, the system automatically strips ampersand characters, allowing an application to use the same string as both a menu item and as text in a tool tip control.|  
  
 A tool tip control has the `WS_POPUP` and **WS_EX_TOOLWINDOW** window styles, regardless of whether you specify them when creating the control.  
  
 To create a tool tip control with extended windows styles, call [CToolTipCtrl::CreateEx](../vs140/CToolTipCtrl--CreateEx.md) instead of **Create**.  
  
## Example  
 See the example for [CPropertySheet::GetTabControl](../vs140/CPropertySheet--GetTabControl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::CToolTipCtrl](../vs140/CToolTipCtrl--CToolTipCtrl.md)