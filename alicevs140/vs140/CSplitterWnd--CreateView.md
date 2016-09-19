---
title: "CSplitterWnd::CreateView"
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
ms.assetid: 1e0909b1-c66b-498d-b065-e59ad3a268a5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::CreateView
Creates the panes for a static splitter window.  
  
## Syntax  
  
```  
  
      virtual BOOL CreateView(  
   int row,  
   int col,  
   CRuntimeClass* pViewClass,  
   SIZE sizeInit,  
   CCreateContext* pContext   
);  
```  
  
#### Parameters  
 `row`  
 Specifies the splitter window row in which to place the new view.  
  
 `col`  
 Specifies the splitter window column in which to place the new view.  
  
 `pViewClass`  
 Specifies the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) of the new view.  
  
 *sizeInit*  
 Specifies the initial size of the new view.  
  
 `pContext`  
 A pointer to a creation context used to create the view (usually the `pContext` passed into the parent frame's overridden [CFrameWnd::OnCreateClient](../vs140/CFrameWnd--OnCreateClient.md) member function in which the splitter window is being created).  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 All panes of a static splitter window must be created before the framework displays the splitter.  
  
 The framework also calls this member function to create new panes when the user of a dynamic splitter window splits a pane, row, or column.  
  
## Example  
 [!CODE [NVC_MFCWindowing#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#4)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::Create](../vs140/CSplitterWnd--Create.md)