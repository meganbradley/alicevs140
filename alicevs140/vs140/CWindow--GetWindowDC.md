---
title: "CWindow::GetWindowDC"
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
ms.assetid: 1b5d4ac6-25dc-4671-ad8f-bc82aa213da7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetWindowDC
Retrieves a device context for the entire window.  
  
## Syntax  
  
```  
  
HDC GetWindowDC() throw();  
```  
  
## Remarks  
 See [GetWindowDC](http://msdn.microsoft.com/library/windows/desktop/dd144947) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#14](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#14)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetDC](../vs140/CWindow--GetDC.md)   
 [CWindow::GetDCEx](../vs140/CWindow--GetDCEx.md)   
 [CWindow::ReleaseDC](../vs140/CWindow--ReleaseDC.md)