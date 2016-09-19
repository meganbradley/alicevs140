---
title: "CMDIFrameWndEx::EnableDocking"
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
ms.assetid: ecd4b4f1-cc3f-4cc2-8960-a429cc1bd7c7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::EnableDocking
Enables docking of the panes that belong to the MDI frame window.  
  
## Syntax  
  
```  
BOOL EnableDocking(  
   DWORD dwDockStyle   
);  
```  
  
#### Parameters  
 [in] `dwDockStyle`  
 Specifies the docking style that you want to apply.  
  
## Return Value  
  
## Remarks  
 Call this function to enable docking of panes that belong to the `CMDIFrameWndEx` object.  
  
## Example  
 The following example shows how the `EnableDocking` method is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#7](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#7)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)