---
title: "CBasePane::GetCurrentAlignment"
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
ms.assetid: 26ded23b-cc43-405e-b222-9cdf41738196
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::GetCurrentAlignment
Returns the current pane alignment.  
  
## Syntax  
  
```  
virtual DWORD GetCurrentAlignment() const;  
```  
  
## Return Value  
 The current alignment of the control bar. The following table shows the possible values:  
  
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
 [CBasePane::SetPaneAlignment](../vs140/CBasePane--SetPaneAlignment.md)