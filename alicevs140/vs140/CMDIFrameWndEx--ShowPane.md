---
title: "CMDIFrameWndEx::ShowPane"
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
ms.assetid: 5a6f8822-77ff-4bc6-a67b-7873640d294b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::ShowPane
Shows or hides the specified pane.  
  
## Syntax  
  
```  
void ShowPane(  
   CBasePane* pBar,  
   BOOL bShow,  
   BOOL bDelay,  
   BOOL bActivate   
);  
```  
  
#### Parameters  
 [in] `pBar`  
 Pointer to the pane to be shown or hidden.  
  
 [in] `bShow`  
 `TRUE` to show the pane. `FALSE` to hide the pane.  
  
 [in] `bDelay`  
 `TRUE` to delay the recalculation of the docking layout. `FALSE` to recalculate the docking layout immediately.  
  
 [in] `bActivate`  
 `TRUE` to show the pane should as active. `FALSE` to show the pane as inactive.  
  
## Remarks  
 Call this method to show or hide the pane. Do not use `ShowWindow` for docking panes.  
  
## Example  
 The following example shows how `ShowPane` is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#16](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#16)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)