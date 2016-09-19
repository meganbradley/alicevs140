---
title: "CWindow::SetScrollRange"
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
ms.assetid: cbc9737b-be33-4ae9-9589-e4cd4c0683ec
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SetScrollRange
Changes the scroll bar range.  
  
## Syntax  
  
```  
  
      BOOL SetScrollRange(  
   int nBar,  
   int nMinPos,  
   int nMaxPos,  
   BOOL bRedraw = TRUE   
) throw();  
```  
  
## Remarks  
 See [SetScrollRange](http://msdn.microsoft.com/library/windows/desktop/bb787599) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetScrollRange](../vs140/CWindow--GetScrollRange.md)