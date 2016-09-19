---
title: "CToolBarCtrl::SetMetrics"
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
ms.assetid: 67789411-50fc-48fc-aa93-f04b06d6ea23
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::SetMetrics
Sets the metrics of the `CToolBarCtrl` object.  
  
## Syntax  
  
```  
  
      void SetMetrics(  
   LPTBMETRICS ptbm   
);  
```  
  
#### Parameters  
 `ptbm`  
 A pointer to the [TBMETRICS](http://msdn.microsoft.com/library/windows/desktop/bb760482) structure of the `CToolBarCtrl` object.  
  
## Remarks  
 This member function emulates the functionality of the [TB_SETMETRICS](http://msdn.microsoft.com/library/windows/desktop/bb787446) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl::GetMetrics](../vs140/CToolBarCtrl--GetMetrics.md)