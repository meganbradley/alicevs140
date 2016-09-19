---
title: "COleControl::SelectStockFont"
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
ms.assetid: 2e1fbe3d-db30-4491-a52e-4deff0a70c7f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SelectStockFont
Selects the stock Font property into a device context.  
  
## Syntax  
  
```  
  
      CFont* SelectStockFont(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 `pDC`  
 The device context into which the font will be selected.  
  
## Return Value  
 A pointer to the previously selected `CFont` object. You should use [CDC::SelectObject](../vs140/CDC--SelectObject.md) to select this font back into the device context when you are finished.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetFont](../vs140/COleControl--GetFont.md)   
 [COleControl::SetFont](../vs140/COleControl--SetFont.md)