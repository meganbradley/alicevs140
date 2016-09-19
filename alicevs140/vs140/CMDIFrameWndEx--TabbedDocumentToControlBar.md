---
title: "CMDIFrameWndEx::TabbedDocumentToControlBar"
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
ms.assetid: e894af24-9c74-4543-a1a9-6f2c67ec2ce7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::TabbedDocumentToControlBar
Converts the specified tabbed document to a docking pane.  
  
## Syntax  
  
```  
virtual BOOL TabbedDocumentToControlBar(  
   CMDIChildWndEx* pMDIChildWnd   
);  
```  
  
#### Parameters  
 `pMDIChildWnd`  
 A pointer to MDI child window that contains a docking pane.  
  
## Return Value  
 `TRUE` if the method was successful, `FALSE` on failure.  
  
## Remarks  
 Use this method to convert a tabbed document to a docking pane. The tabbed document must have been created by using [CMDIFrameWndEx::ControlBarToTabbedDocument](../vs140/CMDIFrameWndEx--ControlBarToTabbedDocument.md).  
  
## Example  
 The following example shows how `TabbedDocumentToControlBar` is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#19](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#19)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)