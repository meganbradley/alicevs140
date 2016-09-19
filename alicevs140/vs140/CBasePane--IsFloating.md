---
title: "CBasePane::IsFloating"
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
ms.assetid: b65a5dc1-2a16-46f7-8a0d-5f40f2c75c4f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsFloating
Determines whether the pane is floating.  
  
## Syntax  
  
```  
virtual BOOL IsFloating() const;  
```  
  
## Return Value  
 `TRUE` if the pane is floating; otherwise, `FALSE`.  
  
## Remarks  
 This method returns the opposite value of [CBasePane::IsDocked](../vs140/CBasePane--IsDocked.md).  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)