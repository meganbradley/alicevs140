---
title: "CMFCTasksPaneTask::SetACCData"
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
ms.assetid: aba3001d-9da8-47d4-9d34-1693c95371f0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPaneTask::SetACCData
Determines the accessibility data for the current task.  
  
## Syntax  
  
```  
virtual BOOL SetACCData(  
    CWnd* pParent,  
    CAccessibilityData& data  
);  
```  
  
#### Parameters  
 [in] `pParent`  
 Represents the parent window of the current task.  
  
 [out] `data`  
 An object of type `CAccessibilityData` that is populated with the accessibility data of the current task.  
  
## Return Value  
 `TRUE` if the `data` parameter was successfully populated with the accessibility data of the current task; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPaneTask Class](../vs140/CMFCTasksPaneTask-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)