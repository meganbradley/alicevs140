---
title: "CMDIChildWndEx::m_dwDefaultTaskbarTabPropertyFlags"
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
ms.assetid: f1cba201-75cc-4984-8586-a5bb78b9120c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::m_dwDefaultTaskbarTabPropertyFlags
A combination of flags, which is passed by the framework to the `SetTaskbarTabProperties` method, when a tab (MDI child) is being registered with Windows 7 taskbar tabs.  
  
## Syntax  
  
```  
AFX_IMPORT_DATA static DWORD m_dwDefaultTaskbarTabPropertyFlags;  
```  
  
## Remarks  
 The default combination is STPF_USEAPPTHUMBNAILWHENACTIVE &#124; STPF_USEAPPPEEKWHENACTIVE.  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)