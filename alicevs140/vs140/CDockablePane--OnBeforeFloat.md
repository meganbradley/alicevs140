---
title: "CDockablePane::OnBeforeFloat"
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
ms.assetid: 6088127a-f396-4cb0-87be-3776db71448c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::OnBeforeFloat
The framework calls this method before a pane transitions to a floating state.  
  
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
 Specifies the docking method. See [CPane::DockPane](../vs140/CPane--DockPane.md) for a list of possible values.  
  
## Return Value  
 `TRUE` if the pane can be floated; otherwise, `FALSE`.  
  
## Remarks  
 This method is called by the framework when a pane is about to float. You can override this method in a derived class if you want to perform any processing before the pane floats.  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPane::OnBeforeFloat](../vs140/CPane--OnBeforeFloat.md)