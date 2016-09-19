---
title: "CMFCToolBar::SetButtonInfo"
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
ms.assetid: 55342a85-6a4f-4214-b4a2-9e22fdeaa6fa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetButtonInfo
Sets the command ID, style, and image ID of a toolbar button.  
  
## Syntax  
  
```  
void SetButtonInfo(  
   int nIndex,  
   UINT nID,  
   UINT nStyle,  
   int iImage   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 The zero-based index of the button whose properties are set.  
  
 [in] `nID`  
 The command ID of the button.  
  
 [in] `nStyle`  
 The style of the button. See [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md) for the list of available toolbar button styles.  
  
 [in] `iImage`  
 The zero-based image index of the button (that is, the index in the collection of toolbar images).  
  
## Remarks  
 Call this method to set the properties of a toolbar button.  
  
 In Debug builds, this method generates an assertion failure if the index that is specified by `nIndex` is invalid.  
  
 Call the [CMFCToolBar::SetButtonStyle](../vs140/CMFCToolBar--SetButtonStyle.md) method to set only the style of the button.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md)   
 [CMFCToolBar::SetButtonStyle](../vs140/CMFCToolBar--SetButtonStyle.md)