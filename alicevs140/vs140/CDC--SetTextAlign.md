---
title: "CDC::SetTextAlign"
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
ms.assetid: b5f47e43-0f47-4dde-a959-892e9cc733d4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetTextAlign
Sets the text-alignment flags.  
  
## Syntax  
  
```  
  
      UINT SetTextAlign(  
   UINT nFlags   
);  
```  
  
#### Parameters  
 `nFlags`  
 Specifies text-alignment flags. The flags specify the relationship between a point and a rectangle that bounds the text. The point can be either the current position or coordinates specified by a text-output function. The rectangle that bounds the text is defined by the adjacent character cells in the text string. The `nFlags` parameter can be one or more flags from the following three categories. Choose only one flag from each category. The first category affects text alignment in the x-direction:  
  
-   **TA_CENTER** Aligns the point with the horizontal center of the bounding rectangle.  
  
-   **TA_LEFT** Aligns the point with the left side of the bounding rectangle. This is the default setting.  
  
-   **TA_RIGHT** Aligns the point with the right side of the bounding rectangle.  
  
 The second category affects text alignment in the y-direction:  
  
-   **TA_BASELINE** Aligns the point with the base line of the chosen font.  
  
-   **TA_BOTTOM** Aligns the point with the bottom of the bounding rectangle.  
  
-   **TA_TOP** Aligns the point with the top of the bounding rectangle. This is the default setting.  
  
 The third category determines whether the current position is updated when text is written:  
  
-   **TA_NOUPDATECP** Does not update the current position after each call to a text-output function. This is the default setting.  
  
-   **TA_UPDATECP** Updates the current x-position after each call to a text-output function. The new position is at the right side of the bounding rectangle for the text. When this flag is set, the coordinates specified in calls to the `TextOut` member function are ignored.  
  
## Return Value  
 The previous text-alignment setting, if successful. The low-order byte contains the horizontal setting and the high-order byte contains the vertical setting; otherwise 0.  
  
## Remarks  
 The `TextOut` and `ExtTextOut` member functions use these flags when positioning a string of text on a display or device. The flags specify the relationship between a specific point and a rectangle that bounds the text. The coordinates of this point are passed as parameters to the `TextOut` member function. The rectangle that bounds the text is formed by the adjacent character cells in the text string.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::ExtTextOut](../vs140/CDC--ExtTextOut.md)   
 [CDC::GetTextAlign](../vs140/CDC--GetTextAlign.md)   
 [CDC::TabbedTextOut](../vs140/CDC--TabbedTextOut.md)   
 [CDC::TextOut](../vs140/CDC--TextOut.md)   
 [SetTextAlign](http://msdn.microsoft.com/library/windows/desktop/dd145091)