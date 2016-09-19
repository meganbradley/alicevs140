---
title: "CPane::GetBorders"
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
ms.assetid: 007ce3b7-92a1-4e66-83e4-e47df325de38
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::GetBorders
Returns the width of the borders of the pane.  
  
## Syntax  
  
```  
CRect GetBorders() const;  
```  
  
## Return Value  
 A [CRect](../vs140/CRect-Class.md) object that contains the current width, in pixels, of each side of the pane. For example, the value of the `left` member of the `CRect` object is the width of the left border.  
  
## Remarks  
 To set the size of the borders, call [CPane::SetBorders](../vs140/CPane--SetBorders.md).  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)