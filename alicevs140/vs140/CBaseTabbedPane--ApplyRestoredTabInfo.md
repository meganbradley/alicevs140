---
title: "CBaseTabbedPane::ApplyRestoredTabInfo"
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
ms.assetid: 2af63720-b425-451b-95d7-7982fe189911
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::ApplyRestoredTabInfo
Loads tab settings from the registry and applies them to a tabbed pane.  
  
## Syntax  
  
```  
virtual void ApplyRestoredTabInfo(  
    BOOL bUseTabIndexes = FALSE  
);  
```  
  
#### Parameters  
 [in] `bUseTabIndexes`  
 This parameter is used internally by the framework.  
  
## Remarks  
 This method is called by the framework when it reloads docking state information from the registry. The method obtains information about tab order and tab names for a tabbed pane.  
  
## Requirements  
 **Header:** afxBaseTabbedPane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)