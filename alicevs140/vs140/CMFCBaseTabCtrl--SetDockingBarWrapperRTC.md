---
title: "CMFCBaseTabCtrl::SetDockingBarWrapperRTC"
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
ms.assetid: 85302b1a-0d36-4a86-9917-505fe593d3b8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::SetDockingBarWrapperRTC
Sets the wrapper class that is used for any objects that are not derived from the [CDockablePane Class](../vs140/CDockablePane-Class.md).  
  
## Syntax  
  
```  
void SetDockingBarWrapperRTC(  
   CRuntimeClass* pRTC   
);  
```  
  
#### Parameters  
 [in] `pRTC`  
 The runtime class information for the new wrapper class.  
  
## Remarks  
 You add tabs to a tab control by using the methods [CMFCBaseTabCtrl::AddTab](../vs140/CMFCBaseTabCtrl--AddTab.md) and [CMFCBaseTabCtrl::InsertTab](../vs140/CMFCBaseTabCtrl--InsertTab.md). When you add a tab, each control on that tab must be dockable. Any objects that are not derived from `CDockablePane` must be wrapped. `AddTab` and `InsertTab` create a wrapper for these objects. The default wrapper class is the [CDockablePaneAdapter Class](../vs140/CDockablePaneAdapter-Class.md). The method `SetDockingBarWrapperRTC` enables you to change the class that is used as a wrapper class. The wrapper class that you provide must be derived from `CDockablePaneAdapter`.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [CDockablePaneAdapter Class](../vs140/CDockablePaneAdapter-Class.md)