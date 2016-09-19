---
title: "CMDIFrameWndEx::EnableAutoHidePanes"
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
ms.assetid: 02895d77-cd54-4d4a-ae70-4673206d67cb
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::EnableAutoHidePanes
Enables auto-hide mode for panes when they are docked at the specified sides of the main frame window.  
  
## Syntax  
  
```  
BOOL EnableAutoHidePanes(  
   DWORD dwDockStyle   
);  
```  
  
#### Parameters  
 [in] `dwDockStyle`  
 Specifies the sides of the main frame window that will be enabled. Use one or more of the following flags.  
  
-   `CBRS_ALIGN_LEFT`  
  
-   `CBRS_ALIGN_RIGHT`  
  
-   `CBRS_ALIGN_TOP`  
  
-   `CBRS_ALIGN_BOTTOM`  
  
## Return Value  
 Call this function to enable auto-hide mode for panes when they are docked at the specified sides of the main frame window.  
  
## Example  
 The following example shows how the `EnableAutoHidePanes` method is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#6](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#6)]  
  
## Remarks  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)