---
title: "CMFCColorPickerCtrl::SetHLS"
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
ms.assetid: da610b8a-601e-49cd-80dc-6739394a28fb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorPickerCtrl::SetHLS
Sets the current color to the specified HLS color value.  
  
## Syntax  
  
```  
void SetHLS(  
   double hue,  
   double luminance,  
   double saturation,  
   BOOL bInvalidate=TRUE   
);  
```  
  
#### Parameters  
 [in] `hue`  
 A hue value.  
  
 [in] `luminance`  
 A luminance value.  
  
 [in] `saturation`  
 A saturation value.  
  
 [in] `bInvalidate`  
 `TRUE` to force the window to immediately update to the new color; otherwise, `FALSE`. The default is `TRUE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxcolorpickerctrl.h  
  
## See Also  
 [CMFCColorPickerCtrl Class](../vs140/CMFCColorPickerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)