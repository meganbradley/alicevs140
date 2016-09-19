---
title: "WM_ Message Handlers: F - K"
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
ms.topic: article
ms.assetid: 0e7de191-1499-499f-859c-62742797808e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WM_ Message Handlers: F - K
The following map entries on the left correspond to the function prototypes on the right:  
  
|Map entry|Function prototype|  
|---------------|------------------------|  
|ON_WM_FONTCHANGE()|afx_msg void [OnFontChange](../vs140/CWnd--OnFontChange.md)();|  
|ON_WM_GETDLGCODE()|afx_msg UINT [OnGetDlgCode](../vs140/CWnd--OnGetDlgCode.md)();|  
|ON_WM_GETMINMAXINFO()|afx_msg void [OnGetMinMaxInfo](../vs140/CWnd--OnGetMinMaxInfo.md)(LPPOINT);|  
|ON_WM_HELPINFO()|afx_msg BOOL [OnHelpInfo](../vs140/CWnd--OnHelpInfo.md)(HELPINFO*);|  
|ON_WM_HOTKEY()|afx_msg void [OnHotKey](../vs140/CWnd--OnHotKey.md)(UINT, UINT, UINT);|  
|ON_WM_HSCROLL()|afx_msg void [OnHScroll](../vs140/CWnd--OnHScroll.md)(UINT, UINT, CWnd*);|  
|ON_WM_HSCROLLCLIPBOARD()|afx_msg void [OnHScrollClipboard](../vs140/CWnd--OnHScrollClipboard.md)(CWnd*, UINT, UINT);|  
|ON_WM_ICONERASEBKGND()|afx_msg void [OnIconEraseBkgnd](../vs140/CWnd--OnIconEraseBkgnd.md)(CDC*);|  
|ON_WM_INITMENU()|afx_msg void [OnInitMenu](../vs140/CWnd--OnInitMenu.md)(CMenu*);|  
|ON_WM_INITMENUPOPUP()|afx_msg void [OnInitMenuPopup](../vs140/CWnd--OnInitMenuPopup.md)(CMenu*, UINT, BOOL);|  
|ON_WM_INPUT()|afx_msg void [OnRawInput](../vs140/CWnd--OnRawInput.md)(UINT, HRAWINPUT);|  
|ON_WM_INPUT_DEVICE_CHANGE()|afx_msg void [OnInputDeviceChange](../vs140/CWnd--OnInputDeviceChange.md)(unsigned short);|  
|ON_WM_INPUTLANGCHANGE()|afx_msg void [OnInputLangChange](../vs140/CWnd--OnInputLangChange.md)(BYTE, UINT);|  
|ON_WM_INPUTLANGCHANGEREQUEST()|afx_msg void [OnInputLangChangeRequest](../vs140/CWnd--OnInputLangChangeRequest.md)(UINT, HKL);|  
|ON_WM_KEYDOWN()|afx_msg void [OnKeyDown](../vs140/CWnd--OnKeyDown.md)(UINT, UINT, UINT);|  
|ON_WM_KEYUP()|afx_msg void [OnKeyUp](../vs140/CWnd--OnKeyUp.md)(UINT, UINT, UINT);|  
|ON_WM_KILLFOCUS()|afx_msg void [OnKillFocus](../vs140/CWnd--OnKillFocus.md)(CWnd*);|  
  
## See Also  
 [Message Maps](../vs140/Message-Maps--MFC-.md)   
 [Handlers for WM_ Messages](../vs140/Handlers-for-WM_-Messages.md)