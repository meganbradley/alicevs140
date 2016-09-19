---
title: "CMFCCmdUsageCount::SetOptions"
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
ms.assetid: 10afe085-4c02-4166-afdf-d77959f01c87
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCmdUsageCount::SetOptions
Sets the values of shared `CMFCCmdUsageCount` class data members.  
  
## Syntax  
  
```  
static BOOL __stdcall SetOptions(  
   UINT nStartCount,  
   UINT nMinUsagePercentage  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `nStartCount`|The new initial count of all tracked commands.|  
|[in] `nMinUsagePercentage`|The new minimum usage percentage.|  
  
## Return Value  
 `TRUE` if the method succeeds, `FALSE` if the `nMinUsagePercentage` parameter is larger than or equal to 100.  
  
## Remarks  
 This method sets the shared `CMFCCmdUsageCount` class data members `m_nStartCount` and `m_nMinUsagePercentage` to `nStartCount` and `nMinUsagePercentage`, respectively. `m_nStartCount` is used by the [CMFCCmdUsageCount::HasEnoughInformation](../vs140/CMFCCmdUsageCount--HasEnoughInformation.md) method to determine whether this object has collected the minimum amount of tracking data. `m_nMinUsagePercentage` is used by the [CMFCCmdUsageCount::IsFreqeuntlyUsedCmd](../vs140/CMFCCmdUsageCount--IsFreqeuntlyUsedCmd.md) method to determine whether a given command is frequently used.  
  
 In Debug builds this method generates an assertion failure if the `nMinUsagePercentage` parameter is larger than or equal to 100.  
  
## Requirements  
 **Header:** afxcmdusagecount.h  
  
## See Also  
 [CMFCCmdUsageCount Class](../vs140/CMFCCmdUsageCount-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCCmdUsageCount::HasEnoughInformation](../vs140/CMFCCmdUsageCount--HasEnoughInformation.md)   
 [CMFCCmdUsageCount::IsFreqeuntlyUsedCmd](../vs140/CMFCCmdUsageCount--IsFreqeuntlyUsedCmd.md)