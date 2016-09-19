---
title: "CDC::GetTextColor"
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
ms.assetid: 13b1e59e-a246-49e4-8e4b-c1b100d34e3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetTextColor
Retrieves the current text color.  
  
## Syntax  
  
```  
  
COLORREF GetTextColor( ) const;  
```  
  
## Return Value  
 The current text color as an RGB color value.  
  
## Remarks  
 The text color is the foreground color of characters drawn by using the GDI text-output member functions [TextOut](../vs140/CDC--TextOut.md), [ExtTextOut](../vs140/CDC--ExtTextOut.md), and [TabbedTextOut](../vs140/CDC--TabbedTextOut.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetBkColor](../vs140/CDC--GetBkColor.md)   
 [CDC::GetBkMode](../vs140/CDC--GetBkMode.md)   
 [CDC::SetBkMode](../vs140/CDC--SetBkMode.md)   
 [CDC::SetTextColor](../vs140/CDC--SetTextColor.md)   
 [GetTextColor](http://msdn.microsoft.com/library/windows/desktop/dd144934)