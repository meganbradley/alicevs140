---
title: "CWnd::OnDestroyClipboard"
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
ms.assetid: dc94e325-2859-4870-b232-0640e7b49a57
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnDestroyClipboard
The framework calls this member function for the Clipboard owner when the Clipboard is emptied through a call to the [EmptyClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649037) Windows function.  
  
## Syntax  
  
```  
  
afx_msg void OnDestroyClipboard( );  
```  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [EmptyClipboard](http://msdn.microsoft.com/library/windows/desktop/ms649037)   
 [WM_DESTROYCLIPBOARD](http://msdn.microsoft.com/library/windows/desktop/ms649024)