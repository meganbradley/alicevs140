---
title: "CMFCToolBarDateTimeCtrl::GetByCmd"
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
ms.assetid: ad909a43-3eb1-49df-a6d4-b9cc1af068f4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::GetByCmd
Retrieves the first `CMFCToolBarDateTimeCtrl` object in the application that has the specified command ID.  
  
## Syntax  
  
```  
static CMFCToolBarDateTimeCtrl* __stdcall GetByCmd(  
   UINT uiCmd  
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The command ID of the button to retrieve.  
  
## Return Value  
 The first `CMFCToolBarDateTimeCtrl` object in the application that has the specified command ID, or `NULL` if no `CMFCToolBarDateTimeCtrl` objects have the specified command ID.  
  
## Remarks  
 This shared utility method is used by methods such as [CMFCToolBarDateTimeCtrl::SetTimeAll](../vs140/CMFCToolBarDateTimeCtrl--SetTimeAll.md) and [CMFCToolBarDateTimeCtrl::GetTimeAll](../vs140/CMFCToolBarDateTimeCtrl--GetTimeAll.md) to set or get the time and date of all instances of the time picker control that have a specified command ID.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarDateTimeCtrl::SetTimeAll](../vs140/CMFCToolBarDateTimeCtrl--SetTimeAll.md)   
 [CMFCToolBarDateTimeCtrl::GetTimeAll](../vs140/CMFCToolBarDateTimeCtrl--GetTimeAll.md)