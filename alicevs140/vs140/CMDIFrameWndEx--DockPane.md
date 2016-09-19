---
title: "CMDIFrameWndEx::DockPane"
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
ms.assetid: fb08253d-8e02-4709-8356-3fceb33ab694
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::DockPane
Docks the specified pane to the frame window.  
  
## Syntax  
  
```  
void DockPane(  
   CBasePane* pBar,  
   UINT nDockBarID=0,  
   LPCRECT lpRect=NULL   
);  
```  
  
#### Parameters  
 [in] `pBar`  
 Pointer to the pane to dock.  
  
 [in] `nDockBarID`  
 Specifies which sides of the frame window to dock to.  
  
 [in] `lpRect`  
 Not used.  
  
## Remarks  
 This method docks the specified the pane to one of the sides of the frame window that was specified when [CBasePane::EnableDocking](../vs140/CBasePane--EnableDocking.md) and [CMDIFrameWndEx::EnableDocking](../vs140/CMDIFrameWndEx--EnableDocking.md) were called.  
  
## Example  
 The following example demonstrates the use of the `DockPane` method. This code snippet comes from the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#4](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#4)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)