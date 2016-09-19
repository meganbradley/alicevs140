---
title: "CPane::IsResizable"
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
ms.assetid: a57d6175-7eae-424a-88dc-5bd6607b9ac8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::IsResizable
Specifies whether the pane is resizable.  
  
## Syntax  
  
```  
virtual BOOL IsResizable() const;  
```  
  
## Return Value  
 `TRUE` if the pane is resizable; otherwise, `FALSE`.  
  
## Remarks  
 Base `CPane` objects are not resizable.  
  
 The docking manager uses the resizable flag to determine pane layout. Non-resizable panes are always located at the outer edges of the parent frame.  
  
 Non-resizable panes cannot reside in docking containers.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockablePane::IsResizable](../vs140/CDockablePane--IsResizable.md)   
 [CDockSite::IsResizable](../vs140/CDockSite--IsResizable.md)