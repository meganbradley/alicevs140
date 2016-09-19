---
title: "CStatic::DrawItem"
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
ms.assetid: 9c70ccfc-9afe-4a1a-87e1-db65f775b7b0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatic::DrawItem
Called by the framework to draw an owner-drawn static control.  
  
## Syntax  
  
```  
  
      virtual void DrawItem(   
   LPDRAWITEMSTRUCT lpDrawItemStruct   
);  
```  
  
#### Parameters  
 `lpDrawItemStruct`  
 A pointer to a [DRAWITEMSTRUCT](../vs140/DRAWITEMSTRUCT-Structure.md) structure. The structure contains information about the item to be drawn and the type of drawing required.  
  
## Remarks  
 Override this function to implement drawing for an owner-drawn **CStatic** object (the control has the style **SS_OWNERDRAW**).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CStatic Class](../vs140/CStatic-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)