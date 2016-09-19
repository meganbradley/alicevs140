---
title: "CPane::OnBeforeFloat"
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
ms.assetid: d7ecaf43-ce97-4b8f-bd2d-70ef30c91976
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::OnBeforeFloat
Called by the framework when a pane is about to float.  
  
## Syntax  
  
```  
virtual BOOL OnBeforeFloat(  
    CRect& rectFloat,  
    AFX_DOCK_METHOD dockMethod  
);  
```  
  
#### Parameters  
 [in] `rectFloat`  
 Specifies the position and size of the pane when it is in a floating state.  
  
 [in] `dockMethod`  
 Specifies the docking method of the pane.  
  
## Return Value  
 `TRUE` if the pane can be floated; otherwise, `FALSE`.  
  
## Remarks  
 This method is called by the framework when a pane is about to float. You can override this method in a derived class if you want to perform any processing before the pane finally floats.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)