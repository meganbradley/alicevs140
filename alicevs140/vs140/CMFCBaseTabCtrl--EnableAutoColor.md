---
title: "CMFCBaseTabCtrl::EnableAutoColor"
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
ms.assetid: de35377f-c045-4933-bd2e-64de11d71192
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::EnableAutoColor
Controls whether the framework uses the automatic background colors when drawing a tab.  
  
## Syntax  
  
```  
void EnableAutoColor(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 A Boolean parameter that determines whether the framework uses automatic colors.  
  
## Remarks  
 A tab control has an array of several predefined colors. When the framework uses automatic colors, each tab in a series of tabs is assigned the next color from this array.  
  
 By default, the automatic colors are determined by the library-defined colors. You can provide a custom array of colors by calling [CMFCBaseTabCtrl::SetAutoColors](../vs140/CMFCBaseTabCtrl--SetAutoColors.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::SetAutoColors](../vs140/CMFCBaseTabCtrl--SetAutoColors.md)