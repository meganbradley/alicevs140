---
title: "CMFCPropertyGridToolTipCtrl::Track"
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
ms.assetid: 7d5b489b-b598-4bc4-a67d-d644e091abfb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridToolTipCtrl::Track
Displays the tooltip control.  
  
## Syntax  
  
```  
void Track(  
   CRect rect,  
   const CString& strText  
);  
```  
  
#### Parameters  
 [in] `rect`  
 Specifies the position and size of the tooltip control.  
  
 [in] `strText`  
 Specifies the text to be shown in the tooltip.  
  
## Remarks  
 This method displays the tooltip control at the position and size specified by `rect`. If the position, size, and text have not changed since the last time this method was called, this method has no effect.  
  
## Requirements  
 **Header:** afxpropertygridtooltipctrl.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridToolTipCtrl Class](../vs140/CMFCPropertyGridToolTipCtrl-Class.md)