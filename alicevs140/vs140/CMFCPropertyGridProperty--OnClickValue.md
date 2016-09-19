---
title: "CMFCPropertyGridProperty::OnClickValue"
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
ms.assetid: ff92e419-1cf2-45c5-b1b2-82ddf5dc2e82
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::OnClickValue
Called by a parent property list control when a user clicks the value field of a property.  
  
## Syntax  
  
```  
virtual BOOL OnClickValue(  
   UINT uiMsg,  
   CPoint point   
);  
```  
  
#### Parameters  
 [in] `uiMsg`  
 A mouse message.  
  
 [in] `point`  
 A point, in client coordinates.  
  
## Return Value  
 `TRUE` if the specified mouse message is processed by this method; otherwise, `FALSE`.  
  
## Remarks  
 By default, this method returns `FALSE` if the current property is not editable. Otherwise, the edit or spin control that is associated with this property processes the specified mouse message, and then this method returns `TRUE`.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)