---
title: "CWnd::OpenClipboard"
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
ms.assetid: c4c22fa8-4683-48b5-bf3d-84ca981ac1b3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OpenClipboard
Opens the Clipboard.  
  
## Syntax  
  
```  
  
BOOL OpenClipboard( );  
```  
  
## Return Value  
 Nonzero if the Clipboard is opened via `CWnd`, or 0 if another application or window has the Clipboard open.  
  
## Remarks  
 Other applications will not be able to modify the Clipboard until the [CloseClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649035) Windows function is called.  
  
 The current `CWnd` object will not become the owner of the Clipboard until the [EmptyClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649037) Windows function is called.  
  
## Example  
 [!CODE [NVC_MFCWindowing#111](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#111)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CloseClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649035)   
 [EmptyClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649037)   
 [OpenClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649048)