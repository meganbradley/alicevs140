---
title: "CGlobalUtils::GetPaneAndAlignFromPoint"
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
ms.assetid: 6c6449a8-27c7-4040-8077-bf614aeef839
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGlobalUtils::GetPaneAndAlignFromPoint
[!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
## Syntax  
  
```  
BOOL GetPaneAndAlignFromPoint(  
   CPaneContainerManager& barContainerManager,  
   CPoint pt,  
   CDockablePane** ppTargetControlBar,  
   DWORD& dwAlignment,  
   BOOL& bTabArea,  
   BOOL& bCaption  
);  
```  
  
#### Parameters  
 [in] `barContainerManager`  
  [in] `pt`  
  [out] `ppTargetControlBar`  
  [out] `dwAlignment`  
  [out] `bTabArea`  
  [out] `bCaption`  
  
## Return Value  
  
## Remarks  
  
## Requirements  
 **Header:** afxglobalutils.h  
  
## See Also  
 [CGlobalUtils Class](../vs140/CGlobalUtils-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)