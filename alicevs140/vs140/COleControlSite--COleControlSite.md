---
title: "COleControlSite::COleControlSite"
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
ms.assetid: 25b63af5-36d1-4569-af9d-c21577df6bfa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::COleControlSite
Constructs a new `COleControlSite` object.  
  
## Syntax  
  
```  
  
      explicit COleControlSite(  
   COleControlContainer* pCtrlCont   
);  
```  
  
#### Parameters  
 `pCtrlCont`  
 A pointer to the control's container (which represents the window that hosts the AtiveX control).  
  
## Remarks  
 This function is called by the [COccManager::CreateContainer](../vs140/COccManager--CreateContainer.md) function. For more information on customizing the creation of containers, see [COccManager::CreateSite](../vs140/COccManager--CreateSite.md).  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControlSite::CreateControl](../vs140/COleControlSite--CreateControl.md)