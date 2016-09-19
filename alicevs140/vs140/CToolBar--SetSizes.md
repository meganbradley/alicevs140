---
title: "CToolBar::SetSizes"
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
ms.assetid: b3bb2116-005d-4f34-a99c-5d051a0901d3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::SetSizes
Call this member function to set the toolbar's buttons to the size, in pixels, specified in *sizeButton*.  
  
## Syntax  
  
```  
  
      void SetSizes(  
   SIZE sizeButton,  
   SIZE sizeImage   
);  
```  
  
#### Parameters  
 *sizeButton*  
 The size in pixels of each button.  
  
 `sizeImage`  
 The size in pixels of each image.  
  
## Remarks  
 The `sizeImage` parameter must contain the size, in pixels, of the images in the toolbar's bitmap. The dimensions in *sizeButton* must be sufficient to hold the image plus 7 pixels extra in width and 6 pixels extra in height. This function also sets the toolbar height to fit the buttons.  
  
 Call this member function only for toolbars that do not follow *Windows Interface Guidelines for Software Design* recommendations for button and image sizes.  
  
## Example  
 [!CODE [NVC_MFCListView#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#8)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::LoadBitmap](../vs140/CToolBar--LoadBitmap.md)   
 [CToolBar::SetButtonInfo](../vs140/CToolBar--SetButtonInfo.md)   
 [CToolBar::SetButtons](../vs140/CToolBar--SetButtons.md)