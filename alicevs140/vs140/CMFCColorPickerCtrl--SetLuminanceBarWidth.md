---
title: "CMFCColorPickerCtrl::SetLuminanceBarWidth"
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
ms.assetid: e97d5886-d1b3-430f-a361-7d3e8d060505
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorPickerCtrl::SetLuminanceBarWidth
Sets the width of the luminance bar in the color picker control.  
  
## Syntax  
  
```  
void SetLuminanceBarWidth(  
   int w   
);  
```  
  
#### Parameters  
 [in] `w`  
 The width of the luminance bar measured in pixels.  
  
## Remarks  
 Use this method to resize the luminance bar, which is on the **Custom** tab of the color picker control. The `w` parameter specifies the new width of the luminance bar. The width value is ignored if it exceeds three-fourths of the client area width.  
  
## Requirements  
 **Header:** afxcolorpickerctrl.h  
  
## See Also  
 [CMFCColorPickerCtrl Class](../vs140/CMFCColorPickerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)