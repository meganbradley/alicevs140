---
title: "CPaneContainerManager::InsertPane"
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
ms.assetid: 197dba4d-5863-4b01-b218-543a1341fa1b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneContainerManager::InsertPane
[!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
## Syntax  
  
```  
virtual BOOL InsertPane(  
   CDockablePane* pControlBarToInsert,  
   CDockablePane* pTargetControlBar,  
   DWORD dwAlignment,  
   LPCRECT lpRect = NULL,  
   AFX_DOCK_METHOD dockMethod = DM_UNKNOWN  
);  
```  
  
#### Parameters  
 [in] `pControlBarToInsert`  
  [in] `pTargetControlBar`  
  [in] `dwAlignment`  
  [in] `lpRect`  
  [in] `dockMethod`  
  
## Return Value  
  
## Remarks  
  
## Requirements  
 **Header:** afxpanecontainermanager.h  
  
## See Also  
 [CPaneContainerManager Class](../vs140/CPaneContainerManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)