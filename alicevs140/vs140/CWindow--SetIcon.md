---
title: "CWindow::SetIcon"
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
ms.assetid: c7b5da14-0663-495c-9661-0292cda2ca07
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetIcon
Sets the window's large or small icon to the icon identified by `hIcon`.  
  
## Syntax  
  
```  
  
      HICON SetIcon(  
   HICON hIcon,  
   BOOL bBigIcon = TRUE   
) throw();  
```  
  
#### Parameters  
 `hIcon`  
 [in] The handle to a new icon.  
  
 `bBigIcon`  
 [in] If **TRUE** (the default value), the method sets a large icon. Otherwise, it sets a small icon.  
  
## Return Value  
 The handle to the previous icon.  
  
## Remarks  
 `SetIcon` sends a [WM_SETICON](http://msdn.microsoft.com/library/windows/desktop/ms632643) message to the window.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetIcon](../vs140/CWindow--GetIcon.md)