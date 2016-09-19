---
title: "COleControl::SerializeExtent"
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
ms.assetid: 4573e344-4f90-4f50-9470-85534213481c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SerializeExtent
Serializes or initializes the state of the display space allotted to the control.  
  
## Syntax  
  
```  
  
      void SerializeExtent(  
   CArchive& ar   
);  
```  
  
#### Parameters  
 `ar`  
 A `CArchive` object to serialize to or from.  
  
## Remarks  
 You can improve a control's binary persistence performance by using `SerializeExtent`, `SerializeStockProps`, and `SerializeVersion` to override **COleControl::Serialize**. See the example below. For further information on optimizing initialization, see [ActiveX Controls: Optimization](../vs140/MFC-ActiveX-Controls--Optimization.md).  
  
## Example  
 [!CODE [NVC_MFCAxCtl#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#8)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SerializeStockProps](../vs140/COleControl--SerializeStockProps.md)   
 [COleControl::SerializeVersion](../vs140/COleControl--SerializeVersion.md)