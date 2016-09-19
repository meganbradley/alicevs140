---
title: "CWnd::UpdateWindow"
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
ms.assetid: 8c15f847-c9ca-4cd0-8a89-5ece5eae80e6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::UpdateWindow
Updates the client area by sending a [WM_PAINT](http://msdn.microsoft.com/library/windows/desktop/dd145213) message if the update region is not empty.  
  
## Syntax  
  
```  
  
void UpdateWindow( );  
```  
  
## Remarks  
 The `UpdateWindow` member function sends a `WM_PAINT` message directly, bypassing the application queue. If the update region is empty, `WM_PAINT` is not sent.  
  
## Example  
 [!CODE [NVC_MFCWindowing#124](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#124)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [UpdateWindow](http://msdn.microsoft.com/library/windows/desktop/dd145167)   
 [CWnd::RedrawWindow](../vs140/CWnd--RedrawWindow.md)