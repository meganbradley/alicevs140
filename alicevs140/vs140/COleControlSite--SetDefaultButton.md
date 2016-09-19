---
title: "COleControlSite::SetDefaultButton"
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
ms.assetid: 0ccd85fc-0926-4856-bbe9-330e258ec10d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::SetDefaultButton
Sets the control as the default button.  
  
## Syntax  
  
```  
  
      void SetDefaultButton(  
   BOOL bDefault   
);  
```  
  
#### Parameters  
 `bDefault`  
 Nonzero if the control should become the default button; otherwise zero.  
  
## Remarks  
  
> [!NOTE]
>  The control must have the **OLEMISC_ACTSLIKEBUTTON** status bit set.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControlSite::IsDefaultButton](../vs140/COleControlSite--IsDefaultButton.md)   
 [DECLARE_OLECTLTYPE](../vs140/DECLARE_OLECTLTYPE.md)