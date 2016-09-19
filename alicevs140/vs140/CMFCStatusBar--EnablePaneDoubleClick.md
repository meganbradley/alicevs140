---
title: "CMFCStatusBar::EnablePaneDoubleClick"
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
ms.assetid: 708433c2-63a8-46e5-96ab-e61e72a5d3ea
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCStatusBar::EnablePaneDoubleClick
Enables or disables the handling of mouse double-clicks on the status bar.  
  
## Syntax  
  
```  
void EnablePaneDoubleClick(  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 If `TRUE`, enable the processing of the mouse double-click. Otherwise disable the processing of the mouse double-click.  
  
## Remarks  
 If the status bar is enabled to process double clicks, Windows sends the `WM_COMMAND` notification together with a resource ID to the owner of the status bar every time that the user double clicks on the status bar pane.  
  
## Requirements  
 **Header:** afxstatusbar.h  
  
## See Also  
 [CMFCStatusBar Class](../vs140/CMFCStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)