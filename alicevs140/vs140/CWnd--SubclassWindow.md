---
title: "CWnd::SubclassWindow"
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
ms.assetid: f781f399-51af-4bf9-88bd-efe5cdaae344
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SubclassWindow
Call this member function to "dynamically subclass" a window and attach it to this `CWnd` object.  
  
## Syntax  
  
```  
  
      BOOL SubclassWindow(  
   HWND hWnd   
);  
```  
  
#### Parameters  
 `hWnd`  
 A handle to the window.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 When a window is dynamically subclassed, windows messages will route through the `CWnd`'s message map and call message handlers in the `CWnd`'s class first. Messages that are passed to the base class will be passed to the default message handler in the window.  
  
 This member function attaches the Windows control to a `CWnd` object and replaces the window's **WndProc** and **AfxWndProc** functions. The function stores a pointer to the old **WndProc** in the `CWnd` object.  
  
> [!NOTE]
>  The window must not already be attached to an MFC object when this function is called.  
  
## Example  
 [!CODE [NVC_MFCWindowing#123](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#123)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DefWindowProc](../vs140/CWnd--DefWindowProc.md)   
 [CWnd::SubclassDlgItem](../vs140/CWnd--SubclassDlgItem.md)   
 [CWnd::Attach](../vs140/CWnd--Attach.md)   
 [CWnd::PreSubclassWindow](../vs140/CWnd--PreSubclassWindow.md)   
 [CWnd::UnsubclassWindow](../vs140/CWnd--UnsubclassWindow.md)