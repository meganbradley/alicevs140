---
title: "CSliderCtrl::SetPageSize"
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
ms.assetid: bcb792aa-3010-44c0-a285-b09373b8e3c3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::SetPageSize
Sets the size of the page for a slider control.  
  
## Syntax  
  
```  
  
      int SetPageSize(  
   int nSize   
);  
```  
  
#### Parameters  
 `nSize`  
 The new page size of the slider control.  
  
## Return Value  
 The previous page size.  
  
## Remarks  
 The page size affects how much the slider moves for the **TB_PAGEUP** and **TB_PAGEDOWN** notifications.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::GetPageSize](../vs140/CSliderCtrl--GetPageSize.md)   
 [CSliderCtrl::GetLineSize](../vs140/CSliderCtrl--GetLineSize.md)