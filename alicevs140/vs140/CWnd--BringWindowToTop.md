---
title: "CWnd::BringWindowToTop"
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
ms.assetid: 677e451f-c08e-44e8-a23d-d848b9bacc91
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::BringWindowToTop
Brings `CWnd` to the top of a stack of overlapping windows.  
  
## Syntax  
  
```  
  
void BringWindowToTop( );  
```  
  
## Remarks  
 In addition, `BringWindowToTop` activates pop-up, top-level, and MDI child windows. The `BringWindowToTop` member function should be used to uncover any window that is partially or completely obscured by any overlapping windows.  
  
 This function just calls the Win32 [BringWindowToTop](http://msdn.microsoft.com/library/windows/desktop/ms632673\(v=vs.85\).aspx) function. Call the [SetWindowPos](../vs140/CWnd--SetWindowPos.md) function to change a window's position in the Z-order. The `BringWindowToTop` function does not change the window style to make it a top-level window. For more information, see [What's the difference between HWND_TOP and HWND_TOPMOST?](http://blogs.msdn.com/b/oldnewthing/archive/2005/11/21/495246.aspx)  
  
## Example  
 [!CODE [NVC_MFCWindowing#71](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#71)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [BringWindowToTop](http://msdn.microsoft.com/library/windows/desktop/ms632673)