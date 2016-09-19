---
title: "CMFCTasksPane::EnableWrapLabels"
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
ms.assetid: ee3ac4f1-c819-4601-87a9-aa393a004a48
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::EnableWrapLabels
Enables or disables word wrapping for the text in labels.  
  
## Syntax  
  
```  
void EnableWrapLabels(  
    BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to wrap the text in labels that appear on the task pane; otherwise, `FALSE`.  
  
## Remarks  
 By default, the framework does not wrap the text in labels. When word wrapping is enabled, the text in labels can appear in multiple lines. The label can include line breaking markers such as `\n` and the underline marker `&`.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)