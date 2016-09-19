---
title: "CMDIFrameWndEx::MDITabNewGroup"
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
ms.assetid: 1529f94b-7a8c-418e-b310-4cc2a04e3dfa
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::MDITabNewGroup
Creates a new tabbed group that has a single window.  
  
## Syntax  
  
```  
void MDITabNewGroup(  
   BOOL bVert=TRUE   
);  
```  
  
#### Parameters  
 [in] `bVert`  
 Specifies the new group alignment. If `TRUE`, the new group is aligned vertically. If `FALSE`, the new group is aligned horizontally.  
  
## Remarks  
 Use this function to create a new tabbed window (new tabbed group) and add the first tab to it.  
  
## Example  
 The following example shows how `MDITabNewGroup` is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#12](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#12)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)