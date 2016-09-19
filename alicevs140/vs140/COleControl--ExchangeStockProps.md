---
title: "COleControl::ExchangeStockProps"
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
ms.assetid: 0973f25d-aaf4-4d1c-87e5-1055ae40dbaa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ExchangeStockProps
Serializes or initializes the state of the control's stock properties.  
  
## Syntax  
  
```  
  
      void ExchangeStockProps(  
   CPropExchange* pPX   
);  
```  
  
#### Parameters  
 `pPX`  
 A pointer to a [CPropExchange](../vs140/CPropExchange-Class.md) object. The framework supplies this object to establish the context of the property exchange, including its direction.  
  
## Remarks  
 This function is normally called by the default implementation of `COleControl::DoPropExchange`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)