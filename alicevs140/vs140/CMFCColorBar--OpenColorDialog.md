---
title: "CMFCColorBar::OpenColorDialog"
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
ms.assetid: bc69d08a-1e5d-4631-9f95-d856b869445b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::OpenColorDialog
Opens a color dialog box.  
  
## Syntax  
  
```  
virtual BOOL OpenColorDialog(  
   const COLORREF colorDefault,  
   COLORREF& colorRes   
);  
```  
  
#### Parameters  
 [in] `colorDefault`  
 The color that is selected by default when the color dialog box opens.  
  
 [out] `colorRes`  
 The color that a user selected.  
  
## Return Value  
 `TRUE` if the user selected a color; `FALSE` if the user canceled the color dialog box.  
  
## Remarks  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)   
 [CMFCColorBar::EnableOtherButton](../vs140/CMFCColorBar--EnableOtherButton.md)