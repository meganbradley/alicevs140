---
title: "CMFCBaseTabCtrl::DetachTab"
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
ms.assetid: 986fb759-9f69-41f9-94b7-9de9b7491433
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::DetachTab
The framework calls this method to detach a tab from the tab control.  
  
## Syntax  
  
```  
virtual BOOL DetachTab(  
   AFX_DOCK_METHOD dockMethod,  
   int nTabNum = -1,  
   BOOL bHide = FALSE  
);  
```  
  
#### Parameters  
 [in] `dockMethod`  
 An enumerated data type provided by the [CBasePane Class](../vs140/CBasePane-Class.md). This data type specifies the method that was used to detach the tab.  
  
 [in] `nTabNum`  
 The zero-based index of the tab to be detached.  
  
 [in] `bHide`  
 A Boolean parameter that indicates whether the framework should hide the detached tab.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 If the tab specified by `nTabNum` is non-detachable, this function fails and returns `FALSE`.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)