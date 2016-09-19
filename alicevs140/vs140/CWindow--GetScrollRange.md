---
title: "CWindow::GetScrollRange"
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
ms.assetid: 6bda6c73-1632-4ee2-aff5-f3c41a2e3dd4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetScrollRange
Retrieves the scroll bar range.  
  
## Syntax  
  
```  
  
      BOOL GetScrollRange(  
   int nBar,  
   LPINT lpMinPos,  
   LPINT lpMaxPos   
) const throw();  
```  
  
## Remarks  
 See [GetScrollRange](http://msdn.microsoft.com/library/windows/desktop/bb787587) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SetScrollRange](../vs140/CWindow--SetScrollRange.md)