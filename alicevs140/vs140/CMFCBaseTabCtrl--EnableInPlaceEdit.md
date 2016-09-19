---
title: "CMFCBaseTabCtrl::EnableInPlaceEdit"
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
ms.assetid: 6e9a263b-8771-4132-a400-0399df227f97
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::EnableInPlaceEdit
Enables direct editing of the tab labels by the user.  
  
## Syntax  
  
```  
virtual void EnableInPlaceEdit(  
   BOOL bEnable   
) = 0;  
```  
  
#### Parameters  
 [in] `bEnable`  
 A Boolean parameter that specifies whether to enable direct editing of the tab labels.  
  
## Remarks  
 By default, direct editing of the tab labels is disabled for tab controls.  
  
 You can enable direct editing for a subset of the tabs on the tab control. To do this, override the method `CMFCBaseTabCtrl::StartRenameTab`. `StartRenameTab` should return a nonzero value for all tabs that support direct editing of tab labels.  
  
 In the [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md), this method is a pure virtual function and has no implementation. If you derive a class from `CMFCBaseTabCtrl`, you must implement this function.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)