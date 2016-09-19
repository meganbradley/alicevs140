---
title: "CColorDialog::SetCurrentColor"
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
ms.assetid: eb1cf2ca-2725-4bbc-94ee-eba6bb40ccf2
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CColorDialog::SetCurrentColor
Call this function after calling `DoModal` to force the current color selection to the color value specified in `clr`.  
  
## Syntax  
  
```  
  
      void SetCurrentColor(  
   COLORREF clr   
);  
```  
  
#### Parameters  
 `clr`  
 An RGB color value.  
  
## Remarks  
 This function is called from within a message handler or `OnColorOK`. The dialog box will automatically update the user's selection based on the value of the `clr` parameter.  
  
## Example  
 See the example for [CColorDialog::OnColorOK](../vs140/CColorDialog--OnColorOK.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CColorDialog Class](../vs140/CColorDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CColorDialog::GetColor](../vs140/CColorDialog--GetColor.md)   
 [CColorDialog::OnColorOK](../vs140/CColorDialog--OnColorOK.md)