---
title: "CWindow::GetUpdateRgn"
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
ms.assetid: 91fd278c-d3b8-4164-ada3-9b4f0135e3c5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetUpdateRgn
Retrieves the update region and copies it into a specified region.  
  
## Syntax  
  
```  
  
      int GetUpdateRgn(  
   HRGN hRgn,  
   BOOL bErase = FALSE   
) throw();  
```  
  
## Remarks  
 See [GetUpdateRgn](http://msdn.microsoft.com/library/windows/desktop/dd144944) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetUpdateRect](../vs140/CWindow--GetUpdateRect.md)