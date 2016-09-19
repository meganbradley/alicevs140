---
title: "CGlobalUtils::CalcExpectedDockedRect"
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
ms.assetid: d8723c0c-c87d-4729-a2d0-9189379f37a1
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGlobalUtils::CalcExpectedDockedRect
[!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
## Syntax  
  
```  
void CalcExpectedDockedRect(  
   CPaneContainerManager& barContainerManager,  
   CWnd* pWndTodock,  
   CPoint ptMouse,  
   CRect& rectResult,  
   BOOL& bDrawTab,  
   CDockablePane** ppTargetBar  
);  
```  
  
#### Parameters  
 [in] `barContainerManager`  
  [in] `pWndTodock`  
  [in] `ptMouse`  
  [out] `rectResult`  
  [out] `bDrawTab`  
  [out] `ppTargetBar`  
  
## Remarks  
  
## Requirements  
 **Header:** afxglobalutils.h  
  
## See Also  
 [CGlobalUtils Class](../vs140/CGlobalUtils-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)