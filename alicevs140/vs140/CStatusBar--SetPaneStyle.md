---
title: "CStatusBar::SetPaneStyle"
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
ms.assetid: b6eebfcf-c9d9-40f5-a111-1bf2f1c69833
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::SetPaneStyle
Call this member function to set the style of a status bar's pane.  
  
## Syntax  
  
```  
  
      void SetPaneStyle(  
   int nIndex,  
   UINT nStyle   
);  
```  
  
#### Parameters  
 `nIndex`  
 Index of the pane whose style is to be set.  
  
 `nStyle`  
 Style of the pane whose style is to be set.  
  
## Remarks  
 A pane's style determines how the pane appears.  
  
 For a list of styles available for status bars, see [SetPaneInfo](../vs140/CStatusBar--SetPaneInfo.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::Create](../vs140/CStatusBar--Create.md)   
 [CStatusBar::GetPaneStyle](../vs140/CStatusBar--GetPaneStyle.md)