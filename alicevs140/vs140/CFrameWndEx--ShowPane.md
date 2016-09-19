---
title: "CFrameWndEx::ShowPane"
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
ms.assetid: 22a9829e-8486-4c74-a99b-6272a0532a4e
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::ShowPane
Shows or hides the specified pane.  
  
## Syntax  
  
```  
void ShowPane(  
   CBasePane* pBar,  
   BOOL bShow,  
   BOOL bDelay,  
   BOOL bActivate  
);  
```  
  
#### Parameters  
 [in] `pBar`  
 A pointer to the control bar to show or hide.  
  
 [in] `bShow`  
 If `TRUE`, the application shows the control bar. Otherwise, the application hides the control bar.  
  
 [in] `bDelay`  
 If `TRUE`, delay the adjustment of the docking layout until the framework calls [AdjustDockingLayout](../vs140/CFrameWndEx--AdjustDockingLayout.md). Otherwise, recalculate the docking layout immediately.  
  
 [in] `bActivate`  
 If `TRUE`, make the control bar active. Otherwise, display the control bar in an inactive state.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)