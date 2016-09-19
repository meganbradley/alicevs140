---
title: "CToolBarCtrl::SetButtonWidth"
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
ms.assetid: 5eda95f6-9ddb-4397-8346-baee0628a324
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetButtonWidth
Sets the minimum and maximum button widths in the toolbar control.  
  
## Syntax  
  
```  
  
      BOOL SetButtonWidth(  
   int cxMin,  
   int cxMax   
);  
```  
  
#### Parameters  
 `cxMin`  
 Minimum button width, in pixels. Toolbar buttons will never be narrower than this value.  
  
 *cxMax*  
 Maximum button width, in pixels. If button text is too wide, the control displays it with ellipsis points.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_SETBUTTONWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb787417), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetButtonInfo](../vs140/CToolBarCtrl--SetButtonInfo.md)