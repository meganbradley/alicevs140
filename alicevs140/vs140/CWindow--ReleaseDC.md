---
title: "CWindow::ReleaseDC"
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
ms.assetid: 8a2d8639-7213-404f-806c-0397b7c28a99
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::ReleaseDC
Releases a device context.  
  
## Syntax  
  
```  
  
      int ReleaseDC(  
   HDC hDC   
);  
```  
  
## Remarks  
 See [ReleaseDC](http://msdn.microsoft.com/library/windows/desktop/dd162920) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#9](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#9)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetDC](../vs140/CWindow--GetDC.md)   
 [CWindow::GetDCEx](../vs140/CWindow--GetDCEx.md)   
 [CWindow::GetWindowDC](../vs140/CWindow--GetWindowDC.md)