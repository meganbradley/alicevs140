---
title: "CAutoHideDockSite::SetOffsetLeft"
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
ms.assetid: 6c815f52-a8dd-4435-926a-12a307084a98
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoHideDockSite::SetOffsetLeft
Sets the margin on the left side of the docking bar.  
  
## Syntax  
  
```  
void SetOffsetLeft(  
   int nOffset   
);  
```  
  
#### Parameters  
 [in] `nOffset`  
 The new offset.  
  
## Remarks  
 [CMFCAutoHideBar](../vs140/CMFCAutoHideBar-Class.md) objects are positioned statically on the [CAutoHideDockSite](../vs140/CAutoHideDockSite-Class.md) object. This means that the user cannot manually change the location of `CMFCAutoHideBar` objects. The `SetOffsetLeft` method controls the spacing between the left side of the left-most `CMFCAutoHideBar` and the left side of the `CAutoHideDockSite`.  
  
## Requirements  
 **Header:** afxautohidedocksite.h  
  
## See Also  
 [CAutoHideDockSite Class](../vs140/CAutoHideDockSite-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)