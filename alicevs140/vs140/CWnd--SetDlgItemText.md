---
title: "CWnd::SetDlgItemText"
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
ms.assetid: 219c44dd-2386-4789-8225-dfd5522db4ec
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetDlgItemText
Sets the caption or text of a control owned by a window or dialog box.  
  
## Syntax  
  
```  
  
      void SetDlgItemText(  
   int nID,  
   LPCTSTR lpszString   
);  
```  
  
#### Parameters  
 `nID`  
 Identifies the control whose text is to be set.  
  
 `lpszString`  
 Points to a [CString](../vs140/CStringT-Class.md) object or null-terminated string that contains the text to be copied to the control.  
  
## Remarks  
 `SetDlgItemText` sends a [WM_SETTEXT](http://msdn.microsoft.com/library/windows/desktop/ms632644) message to the given control.  
  
## Example  
 [!CODE [NVC_MFCWindowing#116](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#116)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [SetDlgItemText](http://msdn.microsoft.com/library/windows/desktop/ms645521)   
 [WM_SETTEXT](http://msdn.microsoft.com/library/windows/desktop/ms632644)   
 [CWnd::GetDlgItemText](../vs140/CWnd--GetDlgItemText.md)