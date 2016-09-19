---
title: "COleControlContainer::COleControlContainer"
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
ms.assetid: 6d42419a-51f8-4ffa-a4a4-45d4c1c09693
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::COleControlContainer
Constructs a `COleControlContainer` object.  
  
## Syntax  
  
```  
  
      explicit COleControlContainer(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 A pointer to the parent window of the control container.  
  
## Remarks  
 Once the object has been successfully created, add a custom control site with a call to `AttachControlSite`.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)