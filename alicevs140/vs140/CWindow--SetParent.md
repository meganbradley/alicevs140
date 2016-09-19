---
title: "CWindow::SetParent"
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
ms.assetid: c810e1af-a55b-47cd-826b-c1b8f38fee2d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetParent
Changes the parent window.  
  
## Syntax  
  
```  
  
      HWND SetParent(  
   HWND hWndNewParent   
) throw();  
```  
  
## Remarks  
 See [SetParent](http://msdn.microsoft.com/library/windows/desktop/ms633541) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#32](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#32)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetParent](../vs140/CWindow--GetParent.md)