---
title: "CMFCRibbonButton::OnClick"
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
ms.assetid: ce30c6aa-2715-433c-898c-262a47a7c206
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonButton::OnClick
Called by the framework when the user clicks the button.  
  
## Syntax  
  
```  
virtual void OnClick(  
   CPoint point   
);  
```  
  
#### Parameters  
 [in] `point`  
 Specifies the position of the mouse click.  
  
## Remarks  
 Override this method in a derived class if you want to handle this event.  
  
## Requirements  
 **Header:** afxribbonbutton.h  
  
## See Also  
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)