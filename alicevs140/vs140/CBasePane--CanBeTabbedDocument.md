---
title: "CBasePane::CanBeTabbedDocument"
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
ms.assetid: 633c64e0-8234-49e8-80f0-4b89ce48c5df
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::CanBeTabbedDocument
Specifies whether the pane can be converted to an MDI tabbed document.  
  
## Syntax  
  
```  
virtual BOOL CanBeTabbedDocument() const;  
```  
  
## Return Value  
 `TRUE` if the pane can be converted to a tabbed document; otherwise, `FALSE`. `CBasePane::CanBeTabbedDocument` always returns `FALSE`.  
  
## Remarks  
 Only objects of certain `CBasePane`-derived types, such as the [CDockablePane Class](../vs140/CDockablePane-Class.md), can be converted to tabbed documents.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)