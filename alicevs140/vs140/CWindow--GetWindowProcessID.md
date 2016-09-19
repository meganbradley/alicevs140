---
title: "CWindow::GetWindowProcessID"
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
ms.assetid: b403eac0-ba9e-4031-8566-f2ba098a4c52
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetWindowProcessID
Retrieves the identifier of the process that created the window.  
  
## Syntax  
  
```  
  
DWORD GetWindowProcessID( ) throw();  
  
```  
  
## Remarks  
 See [GetWindowThreadProcessID](http://msdn.microsoft.com/library/windows/desktop/ms633522) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#15](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#15)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetWindowThreadID](../vs140/CWindow--GetWindowThreadID.md)