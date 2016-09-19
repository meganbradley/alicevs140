---
title: "CWindow::GetStyle"
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
ms.assetid: fe118106-9ae2-4828-9529-7cca5f17dd6d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetStyle
Retrieves the window styles of the window.  
  
## Syntax  
  
```  
  
DWORD GetStyle( ) const throw();  
```  
  
## Return Value  
 The window's styles.  
  
## Remarks  
 To retrieve the extended window styles, call [GetExStyle](../vs140/CWindow--GetExStyle.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#12](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#12)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::ModifyStyle](../vs140/CWindow--ModifyStyle.md)   
 [Window Styles](../vs140/Window-Styles.md)