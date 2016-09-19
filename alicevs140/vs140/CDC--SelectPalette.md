---
title: "CDC::SelectPalette"
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
ms.assetid: d3897fe0-7222-4a7d-bd52-089d2376b29d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SelectPalette
Selects the logical palette that is specified by `pPalette` as the selected palette object of the device context.  
  
## Syntax  
  
```  
  
      CPalette* SelectPalette(  
   CPalette* pPalette,  
   BOOL bForceBackground   
);  
```  
  
#### Parameters  
 `pPalette`  
 Identifies the logical palette to be selected. This palette must already have been created with the `CPalette` member function [CreatePalette](../vs140/CPalette--CreatePalette.md).  
  
 `bForceBackground`  
 Specifies whether the logical palette is forced to be a background palette. If `bForceBackground` is nonzero, the selected palette is always a background palette, regardless of whether the window has the input focus. If `bForceBackground` is 0 and the device context is attached to a window, the logical palette is a foreground palette when the window has the input focus.  
  
## Return Value  
 A pointer to a `CPalette` object identifying the logical palette replaced by the palette specified by `pPalette`. It is **NULL** if there is an error.  
  
## Remarks  
 The new palette becomes the palette object used by GDI to control colors displayed in the device context and replaces the previous palette.  
  
 An application can select a logical palette into more than one device context. However, changes to a logical palette will affect all device contexts for which it is selected. If an application selects a palette into more than one device context, the device contexts must all belong to the same physical device.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::RealizePalette](../vs140/CDC--RealizePalette.md)   
 [CPalette Class](../vs140/CPalette-Class.md)   
 [SelectPalette](http://msdn.microsoft.com/library/windows/desktop/dd162958)