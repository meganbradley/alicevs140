---
title: "CPaneContainerManager::AddPaneContainerManager"
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
ms.assetid: eedc3390-bfb9-44e3-a691-8ad641e086c6
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneContainerManager::AddPaneContainerManager
[!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
## Syntax  
  
```  
virtual BOOL AddPaneContainerManager(  
   CPaneContainerManager& srcManager,  
   BOOL bOuterEdge  
);  
virtual BOOL AddPaneContainerManager(  
   CDockablePane* pTargetControlBar,  
   DWORD dwAlignment,  
   CPaneContainerManager& srcManager,  
   BOOL bCopy  
);  
```  
  
#### Parameters  
 [in] `srcManager`  
  [in] `bOuterEdge`  
  [in] `pTargetControlBar`  
  [in] `dwAlignment`  
  [in] `bCopy`  
  
## Return Value  
  
## Remarks  
  
## Requirements  
 **Header:** afxpanecontainermanager.h  
  
## See Also  
 [CPaneContainerManager Class](../vs140/CPaneContainerManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)