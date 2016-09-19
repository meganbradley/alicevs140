---
title: "COleControl::OnAmbientPropertyChange"
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
ms.assetid: 829a14b3-0aa3-4885-af6d-188b29a73747
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnAmbientPropertyChange
Called by the framework when an ambient property of the container has changed value.  
  
## Syntax  
  
```  
  
      virtual void OnAmbientPropertyChange(  
   DISPID dispid   
);  
```  
  
#### Parameters  
 *dispID*  
 The dispatch ID of the ambient property that changed, or **DISPID_UNKNOWN** if multiple properties have changed.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetAmbientProperty](../vs140/COleControl--GetAmbientProperty.md)