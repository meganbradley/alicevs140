---
title: "CWindow::GetDC"
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
ms.assetid: 25c34628-020f-4c32-a133-a3a09dac2638
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetDC
Retrieves a device context for the client area.  
  
## Syntax  
  
```  
  
HDC GetDC( ) throw();  
```  
  
## Remarks  
 See [GetDC](http://msdn.microsoft.com/library/windows/desktop/dd144871) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#9](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#9)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetDCEx](../vs140/CWindow--GetDCEx.md)   
 [CWindow::GetWindowDC](../vs140/CWindow--GetWindowDC.md)   
 [CWindow::ReleaseDC](../vs140/CWindow--ReleaseDC.md)