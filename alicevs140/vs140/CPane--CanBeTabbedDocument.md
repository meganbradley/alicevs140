---
title: "CPane::CanBeTabbedDocument"
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
ms.assetid: daaed7df-ec72-4202-a7e5-389dfe724866
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::CanBeTabbedDocument
Determines if the pane can be converted to a tabbed document.  
  
## Syntax  
  
```  
virtual BOOL CanBeTabbedDocument() const;  
```  
  
## Return Value  
 `TRUE` if the pane can be converted to a tabbed document; otherwise, `FALSE`.  
  
## Remarks  
 Override this method in a derived class and return `FALSE` if you want to prevent a pane from being converted to a tabbed document. A tabbed document will not be listed in the Window Position menu.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)