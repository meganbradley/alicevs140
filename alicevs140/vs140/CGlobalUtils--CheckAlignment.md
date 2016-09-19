---
title: "CGlobalUtils::CheckAlignment"
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
ms.assetid: 002e7140-3b1c-430d-9b93-d2271d6e7d00
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGlobalUtils::CheckAlignment
[!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
## Syntax  
  
```  
BOOL CheckAlignment(  
   CPoint point,  
   CBasePane* pBar,  
   int nSensitivity,  
   const CDockingManager* pDockManager,  
   BOOL bOuterEdge,  
   DWORD& dwAlignment,  
   DWORD dwEnabledDockBars = CBRS_ALIGN_ANY,  
   LPCRECT lpRectBounds = NULL  
) const;  
```  
  
#### Parameters  
 [in] `point`  
  [in] `pBar`  
  [in] `nSensitivity`  
  [in] `pDockManager`  
  [in] `bOuterEdge`  
  [out] `dwAlignment`  
  [in] `dwEnabledDockBars`  
  [in] `lpRectBounds`  
  
## Return Value  
  
## Remarks  
  
## Requirements  
 **Header:** afxglobalutils.h  
  
## See Also  
 [CGlobalUtils Class](../vs140/CGlobalUtils-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)