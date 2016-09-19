---
title: "COleControl::OnTextChanged"
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
ms.assetid: 535e43da-e65a-4d38-adf7-e7af60c5abd3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnTextChanged
Called by the framework when the stock Caption or Text property value has changed.  
  
## Syntax  
  
```  
  
virtual void OnTextChanged( );  
```  
  
## Remarks  
 The default implementation calls `InvalidateControl`.  
  
 Override this function if you want notification after this property changes.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetText](../vs140/COleControl--SetText.md)   
 [COleControl::InternalGetText](../vs140/COleControl--InternalGetText.md)   
 [COleControl::InvalidateControl](../vs140/COleControl--InvalidateControl.md)