---
title: "CMFCWindowsManagerDialog::CMFCWindowsManagerDialog"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: d6a07dd4-e8f2-45b4-a454-317e86edf25f
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCWindowsManagerDialog::CMFCWindowsManagerDialog
Constructs a [CMFCWindowsManagerDialog](../vs140/CMFCWindowsManagerDialog-Class.md) object.  
  
## Syntax  
  
```  
CMFCWindowsManagerDialog(  
   CMDIFrameWndEx* pMDIFrame,  
   BOOL bHelpButton = FALSE  
);  
```  
  
#### Parameters  
 [in] `pMDIFrame`  
 A pointer to the parent or owner window.  
  
 [in] `bHelpButton`  
 A Boolean parameter that specifies whether the framework displays a **Help** button.  
  
## Remarks  
 For more information about visual managers, see [The Visualization Manager](../vs140/Visualization-Manager.md).  
  
## Requirements  
 **Header:** afxwindowsmanagerdialog.h  
  
## See Also  
 [CMFCWindowsManagerDialog Class](../vs140/CMFCWindowsManagerDialog-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [The Visualization Manager](../vs140/Visualization-Manager.md)