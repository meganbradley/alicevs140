---
title: "CMFCImagePaintArea::SetColor"
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
ms.assetid: 33d62a6a-fa26-4444-9d16-28834f104fa0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCImagePaintArea::SetColor
Sets the current drawing color.  
  
## Syntax  
  
```  
void SetColor(  
   COLORREF color  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `color`|The new drawing color.|  
  
## Remarks  
 When you select a color from the image editor palette bar or color picker, the framework calls this method to update the current drawing color. The initial drawing color is black (a `COLORREF` value of 0).  
  
 The drawing color is used by the image editor dialog box for all drawing modes except for `IMAGE_EDIT_MODE_COLOR`. For more information about drawing modes, see [CMFCImagePaintArea::IMAGE_EDIT_MODE Enumeration](../vs140/CMFCImagePaintArea--IMAGE_EDIT_MODE-Enumeration.md).  
  
## Requirements  
 **Header:** afximagepaintarea.h  
  
## See Also  
 [CMFCImagePaintArea Class](../vs140/CMFCImagePaintArea-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCImagePaintArea::IMAGE_EDIT_MODE Enumeration](../vs140/CMFCImagePaintArea--IMAGE_EDIT_MODE-Enumeration.md)   
 [CMFCImageEditorPaletteBar Class](../vs140/CMFCImageEditorPaletteBar-Class.md)   
 [CMFCImageEditorDialog Class](../vs140/CMFCImageEditorDialog-Class.md)