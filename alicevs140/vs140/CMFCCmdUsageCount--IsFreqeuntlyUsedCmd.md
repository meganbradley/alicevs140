---
title: "CMFCCmdUsageCount::IsFreqeuntlyUsedCmd"
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
ms.assetid: 23fe4d3f-079e-4a15-a80c-f0b37e0bf045
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCmdUsageCount::IsFreqeuntlyUsedCmd
Determines whether the given command is frequently used.  
  
## Syntax  
  
```  
BOOL IsFreqeuntlyUsedCmd(  
   UINT uiCmd  
) const;  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `uiCmd`|Specifies the command to check.|  
  
## Return Value  
 Nonzero if the command is frequently used; otherwise 0.  
  
## Remarks  
 This method returns 0 if the total command usage, `m_nTotalUsage`, is 0. Otherwise, this method returns nonzero if the percentage of which the specified command is used is larger than the minimum percentage, `m_nMinUsagePercentage`. By default, the framework sets the minimum percentage to 5. You can override this value by using the [CMFCCmdUsageCount::SetOptions](../vs140/CMFCCmdUsageCount--SetOptions.md) method. If the minimum percentage is 0, this method returns nonzero if the specified command count is larger than 0.  
  
 [CMFCToolBar::IsCommandRarelyUsed](../vs140/CMFCToolBar--IsCommandRarelyUsed.md) uses this method to determine whether a command is rarely used.  
  
## Requirements  
 **Header:** afxcmdusagecount.h  
  
## See Also  
 [CMFCCmdUsageCount Class](../vs140/CMFCCmdUsageCount-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCCmdUsageCount::SetOptions](../vs140/CMFCCmdUsageCount--SetOptions.md)   
 [CMFCToolBar::IsCommandRarelyUsed](../vs140/CMFCToolBar--IsCommandRarelyUsed.md)