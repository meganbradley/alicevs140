---
title: "CToolBarCtrl::GetMetrics"
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
ms.assetid: 7d3ba9e6-489a-4c57-b27e-caf356f4ede8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetMetrics
Retrieves the metrics of the `CToolBarCtrl` object.  
  
## Syntax  
  
```  
  
      void GetMetrics(  
   LPTBMETRICS ptbm  
) const;  
```  
  
#### Parameters  
 `ptbm`  
 A pointer to the [TBMETRICS](http://msdn.microsoft.com/library/windows/desktop/bb760482) structure of the `CToolBarCtrl` object.  
  
## Remarks  
 This member function emulates the functionality of the [TB_GETMETRICS](http://msdn.microsoft.com/library/windows/desktop/bb787342) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::SetMetrics](../vs140/CToolBarCtrl--SetMetrics.md)