---
title: "CWindow::Attach"
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
ms.assetid: 8f333fe6-ea34-4907-844e-207a86d3acc8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::Attach
Attaches the window identified by `hWndNew` to the `CWindow` object.  
  
## Syntax  
  
```  
  
      void Attach(  
   HWND hWndNew   
) throw();  
```  
  
#### Parameters  
 `hWndNew`  
 [in] The handle to a window.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#1](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#1)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::Detach](../vs140/CWindow--Detach.md)