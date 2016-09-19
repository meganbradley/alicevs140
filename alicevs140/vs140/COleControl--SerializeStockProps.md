---
title: "COleControl::SerializeStockProps"
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
ms.assetid: 96dd06e4-6f41-42d7-ac24-0c1a06a22ab1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SerializeStockProps
Serializes or initializes the state of the `COleControl` stock properties: Appearance, BackColor, BorderStyle, Caption, Enabled, Font, ForeColor, and Text.  
  
## Syntax  
  
```  
  
      void SerializeStockProps(  
   CArchive& ar   
);  
```  
  
#### Parameters  
 `ar`  
 A `CArchive` object to serialize to or from.  
  
## Remarks  
 For a description of stock properties, see [ActiveX Controls: Adding Stock Properties](../vs140/MFC-ActiveX-Controls--Adding-Stock-Properties.md).  
  
 You can improve a control's binary persistence performance by using `SerializeStockProps`, `SerializeExtent`, and `SerializeVersion` to override **COleControl::Serialize**. For an example, see the code at [SerializeExtent](../vs140/COleControl--SerializeExtent.md). For further information on optimizing initialization, see [ActiveX Controls: Optimization](../vs140/MFC-ActiveX-Controls--Optimization.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SerializeExtent](../vs140/COleControl--SerializeExtent.md)   
 [COleControl::SerializeVersion](../vs140/COleControl--SerializeVersion.md)   
 [COleControl::ResetStockProps](../vs140/COleControl--ResetStockProps.md)