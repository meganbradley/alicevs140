---
title: "CSplitterWnd::IdFromRowCol"
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
ms.assetid: 37067267-6bb5-4cb6-b4b9-6f8ac9cae242
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::IdFromRowCol
Obtains the child window ID for the pane at the specified row and column.  
  
## Syntax  
  
```  
  
      int IdFromRowCol(  
   int row,  
   int col   
) const;  
```  
  
#### Parameters  
 `row`  
 Specifies the splitter window row.  
  
 `col`  
 Specifies the splitter window column.  
  
## Return Value  
 The child window ID for the pane.  
  
## Remarks  
 This member function is used for creating nonviews as panes and may be called before the pane exists.  
  
## Example  
 [!CODE [NVC_MFCWindowing#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#5)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::GetPane](../vs140/CSplitterWnd--GetPane.md)   
 [CSplitterWnd::IsChildPane](../vs140/CSplitterWnd--IsChildPane.md)