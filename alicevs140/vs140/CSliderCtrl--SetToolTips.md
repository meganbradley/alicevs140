---
title: "CSliderCtrl::SetToolTips"
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
ms.assetid: 982395f6-5db0-469c-9627-447668f9978a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::SetToolTips
Assigns a tooltip control to a slider control.  
  
## Syntax  
  
```  
  
      void SetToolTips(  
   CToolTipCtrl* pWndTip   
);  
```  
  
#### Parameters  
 `pWndTip`  
 A pointer to a [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) object containing the tooltips to use with the slider control.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TBM_SETTOOLTIPS](http://msdn.microsoft.com/library/windows/desktop/bb760242), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. When a slider control is created with the **TBS_TOOLTIPS** style, it creates a default tooltip control that appears next to the slider, displaying the slider's current position. For a description of the slider control styles, see [Trackbar Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb760147) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::GetToolTips](../vs140/CSliderCtrl--GetToolTips.md)