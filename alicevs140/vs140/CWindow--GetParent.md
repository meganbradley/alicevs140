---
title: "CWindow::GetParent"
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
ms.assetid: bfe5d4de-8620-4e2c-b4ae-498e71fccbe5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetParent
Retrieves the immediate parent window.  
  
## Syntax  
  
```  
  
HWND GetParent( ) const throw();  
```  
  
## Remarks  
 See [GetParent](http://msdn.microsoft.com/library/windows/desktop/ms633510) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#11](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#11)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetParent](../vs140/CWindow--SetParent.md)