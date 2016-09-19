---
title: "CMFCBaseTabCtrl::EnableCustomToolTips"
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
ms.assetid: e8215bd9-f9f7-4bd5-b93a-771797cb274a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::EnableCustomToolTips
Enables custom tooltips for the tab control.  
  
## Syntax  
  
```  
BOOL EnableCustomToolTips(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 A Boolean that determines whether to use custom tooltips.  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Remarks  
 If custom tooltips are enabled, the tab control sends the `AFX_WM_ON_GET_TAB_TOOLTIP` message to the main frame. If you want to support custom tooltips in your application, the main frame window must handle this method and provide the custom tooltip text. For more information about providing custom tooltip text, see [CMFCTabToolTipInfo Class](../vs140/CMFCTabToolTipInfo-Structure.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCTabToolTipInfo Class](../vs140/CMFCTabToolTipInfo-Structure.md)