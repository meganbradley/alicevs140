---
title: "CDC::GetBkColor"
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
ms.assetid: d5511e3b-5a2f-4c92-b506-b13f0fb00695
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetBkColor
Returns the current background color.  
  
## Syntax  
  
```  
  
COLORREF GetBkColor( ) const;  
```  
  
## Return Value  
 An RGB color value.  
  
## Remarks  
 If the background mode is **OPAQUE**, the system uses the background color to fill the gaps in styled lines, the gaps between hatched lines in brushes, and the background in character cells. The system also uses the background color when converting bitmaps between color and monochrome device contexts.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetBkMode](../vs140/CDC--GetBkMode.md)   
 [CDC::SetBkColor](../vs140/CDC--SetBkColor.md)   
 [CDC::SetBkMode](../vs140/CDC--SetBkMode.md)   
 [GetBkColor](http://msdn.microsoft.com/library/windows/desktop/dd144852)