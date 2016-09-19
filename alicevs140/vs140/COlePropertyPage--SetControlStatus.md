---
title: "COlePropertyPage::SetControlStatus"
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
ms.assetid: ea087469-69fe-4e95-9f81-8457f733b130
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertyPage::SetControlStatus
Changes the status of a property page control.  
  
## Syntax  
  
```  
  
      BOOL SetControlStatus(  
   UINT nID,  
   BOOL bDirty   
);  
```  
  
#### Parameters  
 `nID`  
 Contains the ID of a property page control.  
  
 `bDirty`  
 Specifies if a field of the property page has been modified. Set to **TRUE** if the field has been modified, **FALSE** if it has not been modified.  
  
## Return Value  
 **TRUE**, if the specified control was set; otherwise **FALSE**.  
  
## Remarks  
 If the status of a property page control is dirty when the property page is closed or the Apply button is chosen, the control's property will be updated with the appropriate value.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COlePropertyPage Class](../vs140/COlePropertyPage-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertyPage::GetControlStatus](../vs140/COlePropertyPage--GetControlStatus.md)