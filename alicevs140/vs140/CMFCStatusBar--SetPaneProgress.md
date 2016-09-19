---
title: "CMFCStatusBar::SetPaneProgress"
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
ms.assetid: 7176be87-9589-4981-8b9f-5a931db643c5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCStatusBar::SetPaneProgress
Set the current progress indicator of the progress bar for the specified pane.  
  
## Syntax  
  
```  
void SetPaneProgress(  
   int nIndex,  
   long nCurr,  
   BOOL bUpdate=TRUE   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the index of the pane for which to update the progress indicator.  
  
 [in] `nCurr`  
 Specifies the current value of the progress indicator.  
  
 [in] `bUpdate`  
 Specifies whether the pane should be updated immediately.  
  
## Remarks  
 Call this method when you want to update the progress indicator for the progress bar in the specified pane.  
  
 To use this function for the given pane, you must call [CMFCStatusBar::EnablePaneProgressBar](../vs140/CMFCStatusBar--EnablePaneProgressBar.md) first.  
  
## Requirements  
 **Header:** afxstatusbar.h  
  
## See Also  
 [CMFCStatusBar Class](../vs140/CMFCStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)