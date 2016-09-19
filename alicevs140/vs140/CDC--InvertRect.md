---
title: "CDC::InvertRect"
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
ms.assetid: f55adc31-4b36-499a-8de2-f7ea4f440a06
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::InvertRect
Inverts the contents of the given rectangle.  
  
## Syntax  
  
```  
  
      void InvertRect(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `lpRect`  
 Points to a `RECT` that contains the logical coordinates of the rectangle to be inverted. You can also pass a `CRect` object for this parameter.  
  
## Remarks  
 Inversion is a logical NOT operation and flips the bits of each pixel. On monochrome displays, the function makes white pixels black and black pixels white. On color displays, the inversion depends on how colors are generated for the display. Calling `InvertRect` twice with the same rectangle restores the display to its previous colors.  
  
 If the rectangle is empty, nothing is drawn.  
  
## Example  
 [!CODE [NVC_MFCDocView#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#36)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::FillRect](../vs140/CDC--FillRect.md)   
 [InvertRect](http://msdn.microsoft.com/library/windows/desktop/dd145007)   
 [CRect Class](../vs140/CRect-Class.md)   
 [RECT Structure](../vs140/RECT-Structure.md)