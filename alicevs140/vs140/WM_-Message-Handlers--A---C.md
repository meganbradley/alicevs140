---
title: "WM_ Message Handlers: A - C"
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
ms.assetid: 4e315896-d646-4b87-b0ab-41a4a753b045
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WM_ Message Handlers: A - C
The following map entries on the left correspond to the function prototypes on the right:  
  
|Map entry|Function prototype|  
|---------------|------------------------|  
|ON_WM_ACTIVATE()|afx_msg void [OnActivate](../vs140/CWnd--OnActivate.md)(UINT, CWnd*, BOOL);|  
|ON_WM_ACTIVATEAPP()|afx_msg void [OnActivateApp](../vs140/CWnd--OnActivateApp.md)(BOOL, DWORD);|  
|ON_WM_APPCOMMAND()|afx_msg void [OnAppCommand](../vs140/CWnd--OnAppCommand.md)(CWnd*, UINT, UINT, UINT);|  
|ON_WM_ASKCBFORMATNAME()|afx_msg void [OnAskCbFormatName](../vs140/CWnd--OnAskCbFormatName.md)(UINT, LPSTR);|  
|ON_WM_CANCELMODE()|afx_msg void [OnCancelMode](../vs140/CWnd--OnCancelMode.md)();|  
|ON_WM_CAPTURECHANGED()|afx_msg void [OnCaptureChanged](../vs140/CWnd--OnCaptureChanged.md)(CWnd*);|  
|ON_WM_CHANGECBCHAIN()|afx_msg void [OnChangeCbChain](../vs140/CWnd--OnChangeCbChain.md)(HWND, HWND);|  
|ON_WM_CHAR()|afx_msg void [OnChar](../vs140/CWnd--OnChar.md)(UINT, UINT, UINT);|  
|ON_WM_CHARTOITEM()|afx_msg int [OnCharToItem](../vs140/CWnd--OnCharToItem.md)(UINT, CWnd*, UINT);|  
|ON_WM_CHILDACTIVATE()|afx_msg void [OnChildActivate](../vs140/CWnd--OnChildActivate.md)();|  
|ON_WM_CLIPBOARDUPDATE()|afx_msg void [OnClipboardUpdate](../vs140/CWnd--OnClipboardUpdate.md)();|  
|ON_WM_CLOSE()|afx_msg void [OnClose](../vs140/CWnd--OnClose.md)();|  
|ON_WM_COMPACTING()|afx_msg void [OnCompacting](../vs140/CWnd--OnCompacting.md)(UINT);|  
|ON_WM_COMPAREITEM()|afx_msg int [OnCompareItem](../vs140/CWnd--OnCompareItem.md)(LPCOMPAREITEMSTRUCT);|  
|ON_WM_CONTEXTMENU()|afx_msg void [OnContextMenu](../vs140/CWnd--OnContextMenu.md)(CWnd*, CPoint);|  
|ON_WM_COPYDATA()|afx_msg BOOL [OnCopyData](../vs140/CWnd--OnCopyData.md)(CWnd* pWnd, COPYDATASTRUCT\* pCopyDataStruct);|  
|ON_WM_CREATE()|afx_msg int [OnCreate](../vs140/CWnd--OnCreate.md)(LPCREATESTRUCT);|  
|ON_WM_CTLCOLOR()|afx_msg HBRUSH [OnCtlColor](../vs140/CWnd--OnCtlColor.md)(CDC*, CWnd\*, UINT);|  
  
## See Also  
 [Message Maps](../vs140/Message-Maps--MFC-.md)   
 [Handlers for WM_ Messages](../vs140/Handlers-for-WM_-Messages.md)