---
title: "CBasePane::SetPaneAlignment"
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
ms.assetid: 1b4266c4-6a40-4aa4-bfc6-4f8c240fda4e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::SetPaneAlignment
Sets the alignment for the pane.  
  
## Syntax  
  
```  
virtual void SetPaneAlignment(  
   DWORD dwAlignment  
);  
```  
  
#### Parameters  
 [in] `dwAlignment`  
 Specifies the new alignment.  
  
## Remarks  
 Usually, the framework calls this method when a pane is docked from one side of the main frame to another.  
  
 The following table shows the possible values for `dwAlignment`:  
  
|Value|Alignment|  
|-----------|---------------|  
|`CBRS_ALIGN_LEFT`|Left alignment.|  
|`CBRS_ALIGN_RIGHT`|Right alignment.|  
|`CBRS_ALIGN_TOP`|Top alignment.|  
|`CBRS_ALIGN_BOTTOM`|Bottom alignment.|  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBasePane::GetCurrentAlignment](../vs140/CBasePane--GetCurrentAlignment.md)