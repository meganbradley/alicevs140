---
title: "COleControlContainer::OnUIActivate"
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
ms.assetid: 606cf83c-c158-4f02-9099-26a75477a20c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::OnUIActivate
Called by the framework when the control site, pointed to by `pSite`, is about to be activated in-place.  
  
## Syntax  
  
```  
  
      virtual void OnUIActivate(  
   COleControlSite* pSite   
);  
```  
  
#### Parameters  
 `pSite`  
 A pointer to the control site about to be in-place activated.  
  
## Remarks  
 In-place activation means that the container's main menu is replaced with an in-place composite menu.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)