---
title: "CWindow::GetClientRect"
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
ms.assetid: 6a4b12fb-36d3-46d7-8dfd-385d621bc2b8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetClientRect
Retrieves the coordinates of the client area.  
  
## Syntax  
  
```  
  
      BOOL GetClientRect(  
   LPRECT lpRect   
) const throw();  
```  
  
## Remarks  
 See [GetClientRect](http://msdn.microsoft.com/library/windows/desktop/ms633503) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#8](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#8)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetWindowRect](../vs140/CWindow--GetWindowRect.md)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)