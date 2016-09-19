---
title: "CStatusBar::GetPaneStyle"
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
ms.assetid: e75776c3-c1b6-4b57-9c3d-78cce8ecf8c3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::GetPaneStyle
Call this member function to retrieve the style of a status bar's pane.  
  
## Syntax  
  
```  
  
      UINT GetPaneStyle(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Index of the pane whose style is to be retrieved.  
  
## Return Value  
 The style of the status-bar pane specified by `nIndex`.  
  
## Remarks  
 A pane's style determines how the pane appears.  
  
 For a list of styles available for status bars, see [Create](../vs140/CStatusBar--Create.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::Create](../vs140/CStatusBar--Create.md)   
 [CStatusBar::SetPaneStyle](../vs140/CStatusBar--SetPaneStyle.md)