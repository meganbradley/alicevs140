---
title: "CMFCToolBar::SetShowTooltips"
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
ms.assetid: 971e764f-fbc8-47d8-9f9c-f3a8dc72a391
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetShowTooltips
Specifies whether the framework displays tool tips.  
  
## Syntax  
  
```  
static void SetShowTooltips(  
   BOOL bValue   
);  
```  
  
#### Parameters  
 [in] `bValue`  
 If this parameter is `TRUE`, the framework shows tool tips. Otherwise, the framework hides tool tips.  
  
## Remarks  
 By default, the framework shows tool tips.  
  
 Call the [CMFCToolBar::GetShowTooltips](../vs140/CMFCToolBar--GetShowTooltips.md) method to determine whether the framework shows tool tips.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetShowTooltips](../vs140/CMFCToolBar--GetShowTooltips.md)