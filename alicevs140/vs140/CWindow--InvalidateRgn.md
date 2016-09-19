---
title: "CWindow::InvalidateRgn"
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
ms.assetid: bc62778a-84ab-442b-a8d3-f489d97f8739
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::InvalidateRgn
Invalidates the client area within the specified region.  
  
## Syntax  
  
```  
  
      void InvalidateRgn(  
   HRGN hRgn,  
   BOOL bErase = TRUE   
) throw();  
```  
  
## Remarks  
 See [InvalidateRgn](http://msdn.microsoft.com/library/windows/desktop/dd145003) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 Specifies a `void` return type, while the `InvalidateRgn` Win32 function always returns **TRUE**.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::Invalidate](../vs140/CWindow--Invalidate.md)   
 [CWindow::InvalidateRect](../vs140/CWindow--InvalidateRect.md)   
 [CWindow::ValidateRgn](../vs140/CWindow--ValidateRgn.md)