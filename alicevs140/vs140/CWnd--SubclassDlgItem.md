---
title: "CWnd::SubclassDlgItem"
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
ms.assetid: 5a7564b9-310e-472a-8b6e-4e2f22d49b22
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SubclassDlgItem
Call this member function to "dynamically subclass" a control created from a dialog template and attach it to this `CWnd` object.  
  
## Syntax  
  
```  
  
      BOOL SubclassDlgItem(  
   UINT nID,  
   CWnd* pParent   
);  
```  
  
#### Parameters  
 `nID`  
 The control's ID.  
  
 `pParent`  
 The control's parent (usually a dialog box).  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 When a control is dynamically subclassed, windows messages will route through the `CWnd`'s message map and call message handlers in the `CWnd`'s class first. Messages that are passed to the base class will be passed to the default message handler in the control.  
  
 This member function attaches the Windows control to a `CWnd` object and replaces the control's **WndProc** and **AfxWndProc** functions. The function stores the old **WndProc** in the location returned by the `GetSuperWndProcAddr` member function.  
  
## Example  
 [!CODE [NVC_MFCWindowing#122](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#122)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DefWindowProc](../vs140/CWnd--DefWindowProc.md)   
 [CWnd::SubclassWindow](../vs140/CWnd--SubclassWindow.md)   
 [CWnd::Attach](../vs140/CWnd--Attach.md)