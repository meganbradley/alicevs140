---
title: "CDC::SetBkColor"
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
ms.assetid: a553f8ad-83f8-4bbc-ab89-438597421c47
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetBkColor
Sets the current background color to the specified color.  
  
## Syntax  
  
```  
  
      virtual COLORREF SetBkColor(  
   COLORREF crColor   
);  
```  
  
#### Parameters  
 `crColor`  
 Specifies the new background color.  
  
## Return Value  
 The previous background color as an RGB color value. If an error occurs, the return value is 0x80000000.  
  
## Remarks  
 If the background mode is **OPAQUE**, the system uses the background color to fill the gaps in styled lines, the gaps between hatched lines in brushes, and the background in character cells. The system also uses the background color when converting bitmaps between color and monochrome device contexts.  
  
 If the device cannot display the specified color, the system sets the background color to the nearest physical color.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::BitBlt](../vs140/CDC--BitBlt.md)   
 [CDC::GetBkColor](../vs140/CDC--GetBkColor.md)   
 [CDC::GetBkMode](../vs140/CDC--GetBkMode.md)   
 [CDC::SetBkMode](../vs140/CDC--SetBkMode.md)   
 [CDC::StretchBlt](../vs140/CDC--StretchBlt.md)   
 [SetBkColor](http://msdn.microsoft.com/library/windows/desktop/dd162964)