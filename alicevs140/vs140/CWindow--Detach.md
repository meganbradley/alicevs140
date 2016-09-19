---
title: "CWindow::Detach"
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
ms.assetid: f98c4134-2bde-4763-92a6-f082ed8323c5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::Detach
Detaches [m_hWnd](../vs140/CWindow--m_hWnd.md) from the `CWindow` object and sets `m_hWnd` to **NULL**.  
  
## Syntax  
  
```  
  
HWND Detach( ) throw();  
```  
  
## Return Value  
 The `HWND` associated with the `CWindow` object.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#6](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#6)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::Attach](../vs140/CWindow--Attach.md)