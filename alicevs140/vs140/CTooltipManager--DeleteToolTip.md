---
title: "CTooltipManager::DeleteToolTip"
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
ms.assetid: 118d2955-4726-446c-9a36-f679343938e0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTooltipManager::DeleteToolTip
Deletes a tooltip control.  
  
## Syntax  
  
```  
static void DeleteToolTip(  
   CToolTipCtrl*& pToolTip   
);  
```  
  
#### Parameters  
 [in, out] `pToolTip`  
 A reference to a pointer to a tooltip to be destroyed.  
  
## Remarks  
 Call this method for each [CToolTipCtrl](../vs140/CToolTipCtrl-Class.md) that was created by [CTooltipManager::CreateToolTip](../vs140/CTooltipManager--CreateToolTip.md). The parent control should call this method from its `OnDestroy` handler. This is required to correctly remove the tooltip from the framework. This method sets `pToolTip` to `NULL` before it returns.  
  
## Requirements  
 **Header:** afxtooltipmanager.h  
  
## See Also  
 [CTooltipManager Class](../vs140/CTooltipManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)