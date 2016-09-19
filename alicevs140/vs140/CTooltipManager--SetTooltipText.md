---
title: "CTooltipManager::SetTooltipText"
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
ms.assetid: bffebc0e-d176-4e6c-8ef1-dfa0a98decf0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTooltipManager::SetTooltipText
Sets the text and description for a tooltip.  
  
## Syntax  
  
```  
static void SetTooltipText(  
   TOOLINFO* pTI,  
   CToolTipCtrl* pToolTip,  
   UINT nType,  
   const CString strText,  
   LPCTSTR lpszDescr=NULL   
);  
```  
  
#### Parameters  
 [in] `pTI`  
 A pointer to a TOOLINFO object.  
  
 [in, out] `pToolTip`  
 A pointer to the tooltip control for which to set the text and description.  
  
 [in] `nType`  
 Specifies the type of control with which this tooltip is associated.  
  
 [in] `strText`  
 The text to set as the tooltip text.  
  
 [in] `lpszDescr`  
 A pointer to the tooltip description. Can be `NULL`.  
  
## Remarks  
 The value of `nType` must be the same value as the `nType` parameter of [CMFCTooltipManager::CreateToolTip](../vs140/CTooltipManager--CreateToolTip.md) when you created the tooltip.  
  
## Requirements  
 **Header:** afxtooltipmanager.h  
  
## See Also  
 [CTooltipManager Class](../vs140/CTooltipManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)