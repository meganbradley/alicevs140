---
title: "CBaseTabbedPane::RecalcLayout"
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
ms.assetid: fa65abc7-330d-498b-9405-d11c834d771b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::RecalcLayout
Recalculates layout information for the pane.  
  
## Syntax  
  
```  
virtual void RecalcLayout();  
```  
  
## Remarks  
 If the pane is floating, this method notifies the framework to resize the pane to the current size of the mini-frame.  
  
 If the pane is docked, this method does nothing.  
  
## Requirements  
 **Header:** afxbasetabbedpane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)