---
title: "CWindow::GetWindowThreadID"
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
ms.assetid: 31d5aaca-786a-42aa-81a0-5325a0d21fdb
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetWindowThreadID
Retrieves the identifier of the thread that created the specified window.  
  
## Syntax  
  
```  
  
DWORD GetWindowThreadID( ) throw();  
  
```  
  
## Remarks  
 See [GetWindowThreadProcessID](http://msdn.microsoft.com/library/windows/desktop/ms633522) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#16](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#16)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetWindowProcessID](../vs140/CWindow--GetWindowProcessID.md)