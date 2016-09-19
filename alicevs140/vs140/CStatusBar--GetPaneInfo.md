---
title: "CStatusBar::GetPaneInfo"
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
ms.assetid: d55f856a-a755-4fc7-9e04-2ed1321eaa9f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::GetPaneInfo
Sets `nID`, `nStyle`, and `cxWidth` to the ID, style, and width of the indicator pane at the location specified by `nIndex`.  
  
## Syntax  
  
```  
  
      void GetPaneInfo(  
   int nIndex,  
   UINT& nID,  
   UINT& nStyle,  
   int& cxWidth   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Index of the pane whose information is to be retrieved.  
  
 `nID`  
 Reference to a **UINT** that is set to the ID of the pane.  
  
 `nStyle`  
 Reference to a **UINT** that is set to the style of the pane.  
  
 `cxWidth`  
 Reference to an integer that is set to the width of the pane.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::SetPaneInfo](../vs140/CStatusBar--SetPaneInfo.md)   
 [CStatusBar::GetItemID](../vs140/CStatusBar--GetItemID.md)   
 [CStatusBar::GetItemRect](../vs140/CStatusBar--GetItemRect.md)