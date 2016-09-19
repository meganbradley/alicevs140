---
title: "COleControl::ResetStockProps"
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
ms.assetid: 8cf24674-5011-4d66-82e8-44bdaeb8b36b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ResetStockProps
Initializes the state of the `COleControl` stock properties to their default values.  
  
## Syntax  
  
```  
  
void ResetStockProps( );  
```  
  
## Remarks  
 The properties are: Appearance, BackColor, BorderStyle, Caption, Enabled, Font, ForeColor, hWnd, and Text. For a description of stock properties, see [ActiveX Controls: Adding Stock Properties](../vs140/MFC-ActiveX-Controls--Adding-Stock-Properties.md).  
  
 You can improve a control's binary initialization performance by using `ResetStockProps` and `ResetVersion` to override `COleControl::OnResetState`. See the example below. For further information on optimizing initialization, see [ActiveX Controls: Optimization](../vs140/MFC-ActiveX-Controls--Optimization.md).  
  
## Example  
 [!CODE [NVC_MFCAxCtl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#7)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::ResetVersion](../vs140/COleControl--ResetVersion.md)   
 [COleControl::SerializeStockProps](../vs140/COleControl--SerializeStockProps.md)