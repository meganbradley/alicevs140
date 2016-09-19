---
title: "CWnd::GetDlgCtrlID"
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
ms.assetid: b699f911-9e4b-48f8-816c-4b3ff2d6b022
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetDlgCtrlID
Returns the window or control ID value for any child window, not only that of a control in a dialog box.  
  
## Syntax  
  
```  
  
int GetDlgCtrlID( ) const;  
```  
  
## Return Value  
 The numeric identifier of the `CWnd` child window if the function is successful; otherwise 0.  
  
## Remarks  
 Since top-level windows do not have an ID value, the return value of this function is invalid if the `CWnd` is a top-level window.  
  
## Example  
 See the example for [CWnd::OnCtlColor](../vs140/CWnd--OnCtlColor.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetDlgCtrlID](http://msdn.microsoft.com/library/windows/desktop/ms645478)