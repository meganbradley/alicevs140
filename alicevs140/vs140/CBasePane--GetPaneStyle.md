---
title: "CBasePane::GetPaneStyle"
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
ms.assetid: fbf122ee-b472-41c8-a28e-bb126297be60
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::GetPaneStyle
Returns the pane style.  
  
## Syntax  
  
```  
virtual DWORD GetPaneStyle() const;  
```  
  
## Return Value  
 A combination of control bar styles (including CBRS_ styles) that was set by the [CBasePane::SetPaneStyle](../vs140/CBasePane--SetPaneStyle.md) method at creation time.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBasePane::SetPaneStyle](../vs140/CBasePane--SetPaneStyle.md)