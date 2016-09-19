---
title: "CWnd::SetWindowText"
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
ms.assetid: d31d7a10-d215-4e62-80aa-fba2a51effb3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetWindowText
Sets the window's title to the specified text.  
  
## Syntax  
  
```  
  
      void SetWindowText(  
   LPCTSTR lpszString   
);  
```  
  
#### Parameters  
 `lpszString`  
 Points to a [CString](../vs140/CStringT-Class.md) object or null-terminated string to be used as the new title or control text.  
  
## Remarks  
 If the window is a control, the text within the control is set.  
  
 This function causes a [WM_SETTEXT](http://msdn.microsoft.com/library/windows/desktop/ms632644) message to be sent to this window.  
  
## Example  
 [!CODE [NVC_MFCWindowing#121](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#121)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetWindowText](../vs140/CWnd--GetWindowText.md)   
 [SetWindowText](http://msdn.microsoft.com/library/windows/desktop/ms633546)