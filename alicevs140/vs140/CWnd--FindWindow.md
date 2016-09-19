---
title: "CWnd::FindWindow"
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
ms.assetid: 72361c9f-3c21-4a15-b3df-fa91f07d274c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::FindWindow
Returns the top-level `CWnd` whose window class is given by `lpszClassName` and whose window name, or title, is given by `lpszWindowName`.  
  
## Syntax  
  
```  
  
      static CWnd* PASCAL FindWindow(  
   LPCTSTR lpszClassName,  
   LPCTSTR lpszWindowName   
);  
```  
  
#### Parameters  
 `lpszClassName`  
 Points to a null-terminated string that specifies the window's class name (a **WNDCLASS** structure). If `lpClassName` is **NULL**, all class names match.  
  
 `lpszWindowName`  
 Points to a null-terminated string that specifies the window name (the window's title). If `lpWindowName` is **NULL**, all window names match.  
  
## Return Value  
 Identifies the window that has the specified class name and window name. It is **NULL** if no such window is found.  
  
 The `CWnd`* may be temporary and should not be stored for later use.  
  
## Remarks  
 This function does not search child windows.  
  
## Example  
 [!CODE [NVC_MFCWindowing#94](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#94)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [FindWindow](http://msdn.microsoft.com/library/windows/desktop/ms633499)