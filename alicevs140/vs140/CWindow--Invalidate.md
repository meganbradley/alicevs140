---
title: "CWindow::Invalidate"
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
ms.assetid: 0aa8c2ab-10ab-4673-8d00-6e75a111b53f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::Invalidate
Invalidates the entire client area.  
  
## Syntax  
  
```  
  
      BOOL Invalidate(  
   BOOL bErase = TRUE   
) throw();  
```  
  
## Remarks  
 See [InvalidateRect](http://msdn.microsoft.com/library/windows/desktop/dd145002) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 Passes **NULL** for the `RECT` parameter to the `InvalidateRect` Win32 function.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#18](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#18)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::InvalidateRect](../vs140/CWindow--InvalidateRect.md)   
 [CWindow::InvalidateRgn](../vs140/CWindow--InvalidateRgn.md)   
 [CWindow::ValidateRect](../vs140/CWindow--ValidateRect.md)   
 [CWindow::ValidateRgn](../vs140/CWindow--ValidateRgn.md)