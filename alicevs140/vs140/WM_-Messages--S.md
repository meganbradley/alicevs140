---
title: "WM_ Messages: S"
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
ms.assetid: 4b9aec79-a98f-4aa0-a3d9-110941b6dcbc
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WM_ Messages: S
The following map entries correspond to the function prototypes.  
  
|Map entry|Function prototype|  
|---------------|------------------------|  
|ON_WM_SETCURSOR( )|afx_msg BOOL [OnSetCursor](../vs140/CWnd--OnSetCursor.md)( CWnd*, UINT, UINT );|  
|ON_WM_SETFOCUS( )|afx_msg void [OnSetFocus](../vs140/CWnd--OnSetFocus.md)( CWnd* );|  
|ON_WM_SETTINGCHANGE( )|afx_msg void [OnSettingChange](../vs140/CWnd--OnSettingChange.md)( UINT uFlags, LPCTSTR lpszSection );|  
|ON_WM_SHOWWINDOW( )|afx_msg void [OnShowWindow](../vs140/CWnd--OnShowWindow.md)( BOOL, UINT );|  
|ON_WM_SIZE( )|afx_msg void [OnSize](../vs140/CWnd--OnSize.md)( UINT, int, int );|  
|ON_WM_SIZECLIPBOARD( )|afx_msg void [OnSizeClipboard](../vs140/CWnd--OnSizeClipboard.md)( CWnd*, HANDLE );|  
|ON_WM_SIZING( )|afx_msg void [OnSizing](../vs140/CWnd--OnSizing.md)( UINT, LPRECT );|  
|ON_WM_SPOOLERSTATUS( )|afx_msg void [OnSpoolerStatus](../vs140/CWnd--OnSpoolerStatus.md)( UINT, UINT );|  
|ON_WM_STYLECHANGED( )|afx_msg void [OnStyleChanged](../vs140/CWnd--OnStyleChanged.md)( int, LPSTYLESTRUCT );|  
|ON_WM_STYLECHANGING( )|afx_msg void [OnStyleChanging](../vs140/CWnd--OnStyleChanging.md)( int, LPSTYLESTRUCT );|  
|ON_WM_SYSCHAR( )|afx_msg void [OnSysChar](../vs140/CWnd--OnSysChar.md)( UINT, UINT, UINT );|  
|ON_WM_SYSCOLORCHANGE( )|afx_msg void [OnSysColorChange](../vs140/CWnd--OnSysColorChange.md)( );|  
|ON_WM_SYSCOMMAND( )|afx_msg void [OnSysCommand](../vs140/CWnd--OnSysCommand.md)( UINT, LONG );|  
|ON_WM_SYSDEADCHAR( )|afx_msg void [OnSysDeadChar](../vs140/CWnd--OnSysDeadChar.md)( UINT, UINT, UINT );|  
|ON_WM_SYSKEYDOWN( )|afx_msg void [OnSysKeyDown](../vs140/CWnd--OnSysKeyDown.md)( UINT, UINT, UINT );|  
|ON_WM_SYSKEYUP( )|afx_msg void [OnSysKeyUp](../vs140/CWnd--OnSysKeyUp.md)( UINT, UINT, UINT );|  
  
## See Also  
 [Message Maps](../vs140/Message-Maps--MFC-.md)   
 [Handlers for WM_ Messages](../vs140/Handlers-for-WM_-Messages.md)