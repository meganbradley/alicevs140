---
title: "CBasePane::ShowPane"
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
ms.assetid: 37cdf8ac-fc48-4138-894e-07d7d070576b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::ShowPane
Shows or hides the pane.  
  
## Syntax  
  
```  
virtual void ShowPane(  
   BOOL bShow,  
   BOOL bDelay,  
   BOOL bActivate  
);  
```  
  
#### Parameters  
 [in] `bShow`  
 Specifies whether to show (`TRUE`) or hide (`FALSE`) a pane.  
  
 [in] `bDelay`  
 If `TRUE`, recalculating the docking layout is delayed.  
  
 [in] `bActivate`  
 If `TRUE`, the pane is active when shown.  
  
## Remarks  
 This method shows or hides a pane. Use this method instead of `ShowWindow` because this method notifies the relevant docking managers about changes in the pane's visibility.  
  
 Use [CBasePane::IsVisible](../vs140/CBasePane--IsVisible.md) to determine the current visibility of a pane.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)