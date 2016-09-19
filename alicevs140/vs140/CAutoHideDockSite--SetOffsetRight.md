---
title: "CAutoHideDockSite::SetOffsetRight"
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
ms.assetid: 94c9ecaf-a6f4-4117-ba7f-be421a77162e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoHideDockSite::SetOffsetRight
Sets the margin on the right side of the docking bar.  
  
## Syntax  
  
```  
void SetOffsetRight(  
   int nOffset   
);  
```  
  
#### Parameters  
 [in] `nOffset`  
 The new offset.  
  
## Remarks  
 [CMFCAutoHideBar](../vs140/CMFCAutoHideBar-Class.md) objects are positioned statically on the [CAutoHideDockSite](../vs140/CAutoHideDockSite-Class.md) object. This means that the user cannot manually change the location of the `CMFCAutoHideBar` objects. The `SetOffsetRight` method controls the spacing between the right side of the right-most `CMFCAutoHideBar` and the right side of the `CAutoHideDockSite`.  
  
## Requirements  
 **Header:** afxautohidedocksite.h  
  
## See Also  
 [CAutoHideDockSite Class](../vs140/CAutoHideDockSite-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)