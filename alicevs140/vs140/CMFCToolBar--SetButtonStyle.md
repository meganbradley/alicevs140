---
title: "CMFCToolBar::SetButtonStyle"
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
ms.assetid: 53cac229-e066-4e21-8dbd-c55d84f5df68
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetButtonStyle
Sets the style of the toolbar button at the given index.  
  
## Syntax  
  
```  
virtual void SetButtonStyle(  
   int nIndex,  
   UINT nStyle   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 The zero-based index of the toolbar button whose style is to be set.  
  
 [in] `nStyle`  
 The style of the button. See [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md) for the list of available toolbar button styles.  
  
## Remarks  
 This method removes the `TBBS_PRESSED` style if `nStyle` is `TBBS_DISABLED` because the user cannot click a disabled button.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md)