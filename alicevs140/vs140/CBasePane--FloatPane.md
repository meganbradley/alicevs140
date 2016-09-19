---
title: "CBasePane::FloatPane"
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
ms.assetid: 950d4f40-a6b0-4d22-9533-76fc4dbf00bf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::FloatPane
Floats the pane.  
  
## Syntax  
  
```  
virtual BOOL FloatPane(  
   CRect rectFloat,  
   AFX_DOCK_METHOD dockMethod=DM_UNKNOWN,  
   bool bShow=true   
);  
```  
  
#### Parameters  
 [in] `rectFloat`  
 Specifies the screen coordinates where the floating pane appears.  
  
 [in] `dockMethod`  
 Specifies the dock method to use to float the pane.  
  
 [in] `bShow`  
 Specifies whether the floating pane is visible (`TRUE`) or hidden (`FALSE`).  
  
## Return Value  
 `TRUE` if the pane was floated successfully; otherwise `FALSE`.  
  
## Remarks  
 Call this method to float a pane at the screen position specified by `rectFloat`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)