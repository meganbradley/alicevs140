---
title: "COleControl::ExchangeExtent"
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
ms.assetid: ac7255d3-8a49-46a1-85c6-efe02dc5e0ee
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ExchangeExtent
Serializes or initializes the state of the control's extent (its dimensions in **HIMETRIC** units).  
  
## Syntax  
  
```  
  
      BOOL ExchangeExtent(  
   CPropExchange* pPX   
);  
```  
  
#### Parameters  
 `pPX`  
 A pointer to a [CPropExchange](../vs140/CPropExchange-Class.md) object. The framework supplies this object to establish the context of the property exchange, including its direction.  
  
## Return Value  
 Nonzero if the function succeeded; 0 otherwise.  
  
## Remarks  
 This function is normally called by the default implementation of `COleControl::DoPropExchange`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)