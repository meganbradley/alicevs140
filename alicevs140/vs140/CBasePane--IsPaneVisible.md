---
title: "CBasePane::IsPaneVisible"
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
ms.assetid: c8b56158-9dc6-4ad2-910f-3b5ab746d67f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsPaneVisible
Specifies whether the `WS_VISIBLE` flag is set for the pane.  
  
## Syntax  
  
```  
BOOL IsPaneVisible() const;  
```  
  
## Return Value  
 `TRUE` if `WS_VISIBLE` is set; otherwise, `FALSE`.  
  
## Remarks  
 Use [CBasePane::IsVisible](../vs140/CBasePane--IsVisible.md) to determine pane visibility.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBasePane::IsVisible](../vs140/CBasePane--IsVisible.md)