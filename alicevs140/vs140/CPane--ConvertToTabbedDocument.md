---
title: "CPane::ConvertToTabbedDocument"
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
ms.assetid: ff147b58-8b5b-4036-bdae-277b638e4dfd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::ConvertToTabbedDocument
Converts a dockable pane to a tabbed document.  
  
## Syntax  
  
```  
virtual void ConvertToTabbedDocument(  
   BOOL bActiveTabOnly = TRUE  
);  
```  
  
#### Parameters  
 [in] `bActiveTabOnly`  
 Not used in `CPane::ConvertToTabbedDocument`.  
  
## Remarks  
 Only dockable panes can be converted to tabbed documents. For information, see [CDockablePane::ConvertToTabbedDocument](../vs140/CDockablePane--ConvertToTabbedDocument.md).  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)