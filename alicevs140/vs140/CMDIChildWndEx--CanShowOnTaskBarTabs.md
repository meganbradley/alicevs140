---
title: "CMDIChildWndEx::CanShowOnTaskBarTabs"
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
ms.assetid: 1dc9fd88-0687-4ace-a2ff-05f91d0c22cb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::CanShowOnTaskBarTabs
Tells the framework whether this MDI child can be displayed on Windows 7 taskbar tabs.  
  
## Syntax  
  
```  
virtual BOOL CanShowOnTaskBarTabs();  
```  
  
## Return Value  
 `TRUE` if the content of the MDI child can be displayed on Windows 7 taskbar thumbnails.  
  
## Remarks  
 Override this method in a derived class and return `FALSE` to disable the appearance of this MDI child on Windows 7 taskbar tabs.  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)