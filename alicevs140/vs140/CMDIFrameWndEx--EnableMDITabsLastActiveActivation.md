---
title: "CMDIFrameWndEx::EnableMDITabsLastActiveActivation"
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
ms.assetid: c3a7e7d8-28e8-4aa0-b8fc-ee1a60ec8a77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::EnableMDITabsLastActiveActivation
Specifies whether the last active tab should be opened when the user closes the current tab.  
  
## Syntax  
  
```  
void EnableMDITabsLastActiveActivation(  
   BOOL bLastActiveTab=TRUE   
);  
```  
  
#### Parameters  
 [in] `bLastActiveTab`  
 If `TRUE`, enable activation of the last active tab. If `FALSE`, disable activation of the last active tab.  
  
## Remarks  
 There are two ways to open a tab when the active tab is closed:  
  
-   Activate the next tab.  
  
-   Activate the previously active tab.  
  
 The default implementation uses the first way.  
  
 Use `EnableMDITabsLastActiveActivation` to enable the second way of tab activation. It emulates the way Windows opens MDI child windows.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)