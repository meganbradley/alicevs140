---
title: "COleControlContainer::GetAmbientProp"
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
ms.assetid: b5d2e1b9-1dbf-4672-85cd-d9c5f9dffd09
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::GetAmbientProp
Retrieves the value of a specified ambient property.  
  
## Syntax  
  
```  
  
      virtual BOOL GetAmbientProp(   
   COleControlSite* pSite,   
   DISPID dispid,   
   VARIANT* pvarResult    
);  
```  
  
#### Parameters  
 `pSite`  
 A pointer to a control site from which the ambient property will be retrieved.  
  
 `dispid`  
 The dispatch ID of the desired ambient property.  
  
 *pVarResult*  
 A pointer to the value of the ambient property.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)