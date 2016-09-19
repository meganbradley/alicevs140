---
title: "CSliderCtrl::GetBuddy"
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
ms.assetid: 0a03c623-0ce0-42c4-a36e-8fb01e6da204
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::GetBuddy
Retrieves the handle to a slider control buddy window at a given location.  
  
## Syntax  
  
```  
  
      CWnd* GetBuddy(  
   BOOL fLocation = TRUE   
) const;  
```  
  
#### Parameters  
 `fLocation`  
 A Boolean value that indicates which of two buddy window handles to retrieve. Can be one of the following values:  
  
-   **TRUE** Retrieves the handle to the buddy to the left of the slider. If the slider control uses the `TBS_VERT` style, the message will retrieve the buddy above the slider.  
  
-   **FALSE** Retrieves the handle to the buddy to the right of the slider. If the slider control uses the `TBS_VERT` style, the message will retrieve the buddy below the slider.  
  
## Return Value  
 A pointer to a [CWnd](../vs140/CWnd-Class.md) object that is the buddy window at the location specified by `fLocation`, or **NULL** if no buddy window exists at that location.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TBM_GETBUDDY](http://msdn.microsoft.com/library/windows/desktop/bb760178), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For a description of the slider control styles, see [Trackbar Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb760147) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::SetBuddy](../vs140/CSliderCtrl--SetBuddy.md)