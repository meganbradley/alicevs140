---
title: "CPaneDivider::AddPaneContainer"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 55f735ac-27f2-4c6e-a5fd-3db80a48e08b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneDivider::AddPaneContainer
[!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
## Syntax  
  
```  
virtual BOOL AddPaneContainer(  
   CPaneContainerManager& barContainerManager,  
   BOOL bOuterEdge  
);  
virtual BOOL AddPaneContainer(  
   CDockablePane* pTargetBar,  
   CPaneContainerManager& barContainerManager,  
   DWORD dwAlignment  
);  
```  
  
#### Parameters  
 [in] `barContainerManager`  
  [in] `bOuterEdge`  
  [in] `pTargetBar`  
  [in] `dwAlignment`  
  
## Return Value  
  
## Remarks  
  
## Requirements  
 **Header:** afxpanedivider.h  
  
## See Also  
 [CPaneDivider Class](../vs140/CPaneDivider-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)