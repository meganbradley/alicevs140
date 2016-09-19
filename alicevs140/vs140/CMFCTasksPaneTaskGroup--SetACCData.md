---
title: "CMFCTasksPaneTaskGroup::SetACCData"
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
ms.assetid: ed77ba2c-a595-4b36-9c7c-1faaa606fa0a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPaneTaskGroup::SetACCData
Determines the accessibility data for the current task group.  
  
## Syntax  
  
```  
virtual BOOL SetACCData(  
    CWnd* pParent,  
    CAccessibilityData& data  
);  
```  
  
#### Parameters  
 [in] `pParent`  
 Represents the parent window of the current task group.  
  
 [out] `data`  
 An object of type `CAccessibilityData` that is populated with the accessibility data of the current task group.  
  
## Return Value  
 `TRUE` if the `data` parameter was successfully populated with the accessibility data of the current task group; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPaneTaskGroup Class](../vs140/CMFCTasksPaneTaskGroup-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)