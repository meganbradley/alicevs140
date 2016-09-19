---
title: "CMDIChildWndEx::CanShowOnWindowsList"
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
ms.assetid: 2e649415-990e-4136-ab83-48786d3d949e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::CanShowOnWindowsList
Specifies whether the MDI child window name can be displayed in the [CMFCWindowsManagerDialog](../vs140/CMFCWindowsManagerDialog-Class.md) dialog box.  
  
## Syntax  
  
```  
virtual BOOL CanShowOnWindowsList();  
```  
  
## Return Value  
 `TRUE` if the window can be displayed in the **Windows** dialog box; otherwise, `FALSE`.  
  
## Remarks  
 Override this method in a derived class and return `FALSE` if the window should not be displayed in the **Windows** dialog box. This function is called from `CMFCWindowsManagerDialog`.  
  
## Requirements  
 **Header:** afxMDIChildWndEx.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)