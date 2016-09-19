---
title: "COccManager::CreateSite"
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
ms.assetid: c3093bc9-796a-492c-920a-32031861c648
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COccManager::CreateSite
Called by the framework to create a control site, hosted by the container pointed to by `pCtrlCont`.  
  
## Syntax  
  
```  
  
      virtual COleControlSite* CreateSite(  
   COleControlContainer* pCtrlCont   
);  
```  
  
#### Parameters  
 `pCtrlCont`  
 A pointer to the control container hosting the new control site.  
  
## Return Value  
 A pointer to the newly created control site.  
  
## Remarks  
 Override this function to create a custom control site, using your [COleControlSite](../vs140/COleControlSite-Class.md)-derived class.  
  
 Each control container can host multiple sites. Create additional sites with multiple calls to `CreateSite`.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COccManager Class](../vs140/COccManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)