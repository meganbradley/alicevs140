---
title: "CPane::SetVirtualRect"
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
ms.assetid: 2ac97ae8-47e7-4aa9-b7db-cdbd996b2edd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::SetVirtualRect
Sets the *virtual rectangle* of the pane.  
  
## Syntax  
  
```  
void SetVirtualRect(  
   const CRect& rect,  
   BOOL bMapToParent = TRUE  
);  
```  
  
#### Parameters  
 [in] `rect`  
 A `CRect` object that specifies the virtual rectangle to be set.  
  
 [in] `bMapToParent`  
 Specify `TRUE` if `rect` contains points relative to the parent window.  
  
## Remarks  
 A *virtual rectangle* stores the original position of a pane when it is moved. The framework can use the virtual rectangle to restore the original position.  
  
 Do not call methods that are related to virtual rectangles unless you are moving panes programmatically.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPane::GetVirtualRect](../vs140/CPane--GetVirtualRect.md)