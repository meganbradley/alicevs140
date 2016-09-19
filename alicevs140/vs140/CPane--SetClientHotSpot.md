---
title: "CPane::SetClientHotSpot"
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
ms.assetid: 1ae72fa7-d670-418e-a49b-4c9fffd6e678
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::SetClientHotSpot
Sets the *hot spot* for the pane.  
  
## Syntax  
  
```  
void SetClientHotSpot(  
   const CPoint& ptNew  
);  
```  
  
#### Parameters  
 [in] `ptNew`  
 A `CPoint` object that specifies the new hot spot.  
  
## Remarks  
 The *hot spot* is the point on the pane that the user selects and holds to move the pane. A hot spot is used for smooth animation when the pane is dragged from a docked position.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPane::GetClientHotSpot](../vs140/CPane--GetClientHotSpot.md)