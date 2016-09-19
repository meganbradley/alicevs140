---
title: "COleControl::OnEnumVerbs"
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
ms.assetid: d2c5abbc-2ab3-4fd4-8643-11e917a5f685
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnEnumVerbs
Called by the framework when the container calls the **IOleObject::EnumVerbs** member function.  
  
## Syntax  
  
```  
  
      virtual BOOL OnEnumVerbs(  
   LPENUMOLEVERB* ppenumOleVerb   
);  
```  
  
#### Parameters  
 `ppenumOleVerb`  
 A pointer to the **IEnumOLEVERB** object that enumerates the control's verbs.  
  
## Return Value  
 Nonzero if verbs are available; otherwise 0.  
  
## Remarks  
 The default implementation enumerates the `ON_OLEVERB` entries in the message map.  
  
 Override this function to change the default way of enumerating verbs.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [ON_OLEVERB](../vs140/ON_OLEVERB.md)   
 [ON_STDOLEVERB](../vs140/ON_STDOLEVERB.md)