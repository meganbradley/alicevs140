---
title: "COleControlContainer::OnUIDeactivate"
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
ms.assetid: a1116961-5b25-4f09-a537-b0bf383f1c54
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::OnUIDeactivate
Called by the framework when the control site, pointed to by `pSite`, is about to be deactivated.  
  
## Syntax  
  
```  
  
      virtual void OnUIDeactivate(  
   COleControlSite* pSite   
);  
```  
  
#### Parameters  
 `pSite`  
 A pointer to the control site about to be deactivated.  
  
## Remarks  
 When this notification is received, the container should reinstall its user interface and take focus.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)