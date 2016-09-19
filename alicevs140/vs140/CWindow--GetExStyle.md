---
title: "CWindow::GetExStyle"
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
ms.assetid: 9e9b2f27-55fb-4da9-9445-bdd4efff9888
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetExStyle
Retrieves the extended window styles of the window.  
  
## Syntax  
  
```  
  
DWORD GetExStyle( ) const throw();  
```  
  
## Return Value  
 The window's extended styles.  
  
## Remarks  
 To retrieve the regular window styles, call [GetStyle](../vs140/CWindow--GetStyle.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#10](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#10)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::ModifyStyleEx](../vs140/CWindow--ModifyStyleEx.md)