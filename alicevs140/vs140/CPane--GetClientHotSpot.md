---
title: "CPane::GetClientHotSpot"
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
ms.assetid: 6e23326f-dbd4-4802-bb22-0a3acae50c3a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::GetClientHotSpot
Returns the *hot spot* for the pane.  
  
## Syntax  
  
```  
CPoint GetClientHotSpot() const;  
```  
  
## Return Value  
  
## Remarks  
 The *hot spot* is the point on the pane that the user selects and holds to move the pane. A hot spot is used for smooth animation when the pane is moved from a docked position.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPane::SetClientHotSpot](../vs140/CPane--SetClientHotSpot.md)