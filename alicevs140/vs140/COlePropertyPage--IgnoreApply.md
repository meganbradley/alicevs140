---
title: "COlePropertyPage::IgnoreApply"
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
ms.assetid: 43078cae-7a9b-4f0b-a8c7-d0f6c9d2ad1b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::IgnoreApply
Determines which controls do not enable the Apply button.  
  
## Syntax  
  
```  
  
      void IgnoreApply(  
   UINT nID   
);  
```  
  
#### Parameters  
 `nID`  
 ID of the control to be ignored.  
  
## Remarks  
 The property page's Apply button is enabled only when values of property page controls have been changed. Use this function to specify controls that do not cause the Apply button to be enabled when their values change.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertyPage::GetControlStatus](../vs140/COlePropertyPage--GetControlStatus.md)