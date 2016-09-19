---
title: "CToolBar::LoadBitmap"
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
ms.assetid: 1bcda32b-58a6-4be6-8857-3e1797a1d4d0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::LoadBitmap
Call this member function to load the bitmap specified by `lpszResourceName` or `nIDResource`.  
  
## Syntax  
  
```  
  
      BOOL LoadBitmap(  
   LPCTSTR lpszResourceName   
);  
BOOL LoadBitmap(  
   UINT nIDResource   
);  
```  
  
#### Parameters  
 `lpszResourceName`  
 Pointer to the resource name of the bitmap to be loaded.  
  
 `nIDResource`  
 Resource ID of the bitmap to be loaded.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The bitmap should contain one image for each toolbar button. If the images are not of the standard size (16 pixels wide and 15 pixels high), call [SetSizes](../vs140/CToolBar--SetSizes.md) to set the button sizes and their images.  
  
> [!WARNING]
>  `CToolBar` supports bitmaps with a maximum of 16 colors. When you load an image into a toolbar editor, Visual Studio automatically converts the image to a 16-color bitmap, if necessary, and displays a warning message if the image was converted. If you use an image with more than 16 colors (using an external editor to edit the image), the application might behave unexpectedly.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::Create](../vs140/CToolBar--Create.md)   
 [CToolBar::SetButtons](../vs140/CToolBar--SetButtons.md)   
 [CToolBar::SetSizes](../vs140/CToolBar--SetSizes.md)   
 [CToolBar::LoadToolBar](../vs140/CToolBar--LoadToolBar.md)