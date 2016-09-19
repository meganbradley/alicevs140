---
title: "CStatusBar::SetIndicators"
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
ms.assetid: e18f1dd8-b5c2-4301-b0e6-34e47f267294
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::SetIndicators
Sets each indicator's ID to the value specified by the corresponding element of the array `lpIDArray`, loads the string resource specified by each ID, and sets the indicator's text to the string.  
  
## Syntax  
  
```  
  
      BOOL SetIndicators(  
   const UINT* lpIDArray,  
   int nIDCount   
);  
```  
  
#### Parameters  
 `lpIDArray`  
 Pointer to an array of IDs.  
  
 `nIDCount`  
 Number of elements in the array pointed to by `lpIDArray`.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::CStatusBar](../vs140/CStatusBar--CStatusBar.md)   
 [CStatusBar::Create](../vs140/CStatusBar--Create.md)   
 [CStatusBar::SetPaneInfo](../vs140/CStatusBar--SetPaneInfo.md)   
 [CStatusBar::SetPaneText](../vs140/CStatusBar--SetPaneText.md)