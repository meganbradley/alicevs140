---
title: "CMFCPropertyGridCtrl::OnChangeSelection"
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
ms.assetid: 56fdef3d-866f-4c16-818a-75d297ee4d3c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::OnChangeSelection
Called by the framework when the current selection is changed.  
  
## Syntax  
  
```  
virtual void OnChangeSelection(  
   CMFCPropertyGridProperty* pNewSel,   
   CMFCPropertyGridProperty* pOldSel   
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `pNewSel`|Pointer to the newly selected property.|  
|[in] `pOldSel`|Pointer to the previously selected property.|  
  
## Remarks  
 The default implementation of this method does nothing.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)