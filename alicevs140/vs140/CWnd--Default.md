---
title: "CWnd::Default"
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
ms.assetid: 6d1914c0-256b-467a-9ddc-1627e87290cf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::Default
Calls the default window procedure.  
  
## Syntax  
  
```  
  
LRESULT Default( );  
```  
  
## Return Value  
 Depends on the message sent.  
  
## Remarks  
 The default window procedure provides default processing for any window message that an application does not process. This member function ensures that every message is processed.  
  
## Example  
 [!CODE [NVC_MFCWindowing#85](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#85)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DefWindowProc](../vs140/CWnd--DefWindowProc.md)   
 [DefWindowProc](http://msdn.microsoft.com/library/windows/desktop/ms633572)