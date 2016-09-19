---
title: "CMFCPropertyGridProperty::OnDblClk"
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
ms.assetid: 4e5799c2-4541-4c33-bdcb-d238c7bcc92c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::OnDblClk
Called by the framework when the user double clicks a property.  
  
## Syntax  
  
```  
virtual BOOL OnDblClk(  
   CPoint point   
);  
```  
  
#### Parameters  
 [in] `point`  
 A point, in client coordinates.  
  
## Return Value  
 `TRUE` if this method is successful; otherwise, `FALSE`.  
  
## Remarks  
 By default, this method selects the next property item in the property list control.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)