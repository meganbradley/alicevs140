---
title: "COlePropertyPage::GetControlStatus"
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
ms.assetid: 0df5e8ba-5784-4c06-9f98-c0e8ac6488fd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::GetControlStatus
Determines whether the user has modified the value of the property page control with the specified resource ID.  
  
## Syntax  
  
```  
  
      BOOL GetControlStatus(  
   UINT nID   
);  
```  
  
#### Parameters  
 `nID`  
 Resource ID of a property page control.  
  
## Return Value  
 **TRUE** if the control value has been modified; otherwise **FALSE**.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertyPage::SetControlStatus](../vs140/COlePropertyPage--SetControlStatus.md)