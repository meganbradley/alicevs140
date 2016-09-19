---
title: "CWnd::GetDlgItem"
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
ms.assetid: 64aa4c0a-6b25-4175-91a0-9957ca07eeab
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetDlgItem
Retrieves a pointer to the specified control or child window in a dialog box or other window.  
  
## Syntax  
  
```  
  
      CWnd* GetDlgItem(  
   int nID   
) const;  
void GetDlgItem(  
   int nID,  
   HWND* phWnd  
) const;  
```  
  
#### Parameters  
 `nID`  
 Specifies the identifier of the control or child window to be retrieved.  
  
 `phWnd`  
 A pointer to a child window.  
  
## Return Value  
 A pointer to the given control or child window. If no control with the integer ID given by the `nID` parameter exists, the value is **NULL**.  
  
 The returned pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 The pointer returned is usually cast to the type of control identified by `nID`.  
  
## Example  
 [!CODE [NVC_MFCWindowing#97](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#97)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetWindow](../vs140/CWnd--GetWindow.md)   
 [CWnd::GetDescendantWindow](../vs140/CWnd--GetDescendantWindow.md)   
 [CWnd::GetWindow](../vs140/CWnd--GetWindow.md)   
 [GetDlgItem](http://msdn.microsoft.com/library/windows/desktop/ms645481)