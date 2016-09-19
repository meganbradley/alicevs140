---
title: "CMFCDesktopAlertWnd::SetTransparency"
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
ms.assetid: efeb08a6-d85b-4617-be22-067b60b39c5d
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDesktopAlertWnd::SetTransparency
Sets the transparency level of the popup window.  
  
## Syntax  
  
```  
void SetTransparency(  
    BYTE nTransparency   
);  
```  
  
#### Parameters  
 [in] `nTransparency`  
 Specifies the transparency level. This value must be between 0 and 255, inclusive. The greater the value, the more opaque the window.  
  
## Remarks  
 Call this function to set the transparency level of the popup window.  
  
## Requirements  
 **Header:** afxDesktopAlertWnd.h  
  
## See Also  
 [CMFCDesktopAlertWnd Class](../vs140/CMFCDesktopAlertWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)