---
title: "COleControl::SetBorderStyle"
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
ms.assetid: fd21609b-5a4f-4c31-be0e-8442f6bd0c0c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetBorderStyle
Sets the stock BorderStyle property value of your control.  
  
## Syntax  
  
```  
  
      void SetBorderStyle(  
   short sBorderStyle   
);  
```  
  
#### Parameters  
 *sBorderStyle*  
 The new border style for the control; 0 indicates no border and 1 indicates a normal border.  
  
## Remarks  
 The control window will then be re-created and `OnBorderStyleChanged` called.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetBorderStyle](../vs140/COleControl--GetBorderStyle.md)   
 [COleControl::OnBorderStyleChanged](../vs140/COleControl--OnBorderStyleChanged.md)