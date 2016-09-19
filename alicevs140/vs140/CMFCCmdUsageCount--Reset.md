---
title: "CMFCCmdUsageCount::Reset"
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
ms.assetid: a62e91ca-9f9a-4816-9100-af0105c815f6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCmdUsageCount::Reset
Clears the usage count of all commands.  
  
## Syntax  
  
```  
void Reset();  
```  
  
## Remarks  
 Call this method to clear all entries from the map structure of command counts, `m_CmdUsage`, and to reset the total command usage, `m_nTotalUsage`, counter to 0.  
  
## Requirements  
 **Header:** afxcmdusagecount.h  
  
## See Also  
 [CMFCCmdUsageCount Class](../vs140/CMFCCmdUsageCount-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)