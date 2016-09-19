---
title: "CMFCPropertyGridProperty::GetOriginalValue"
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
ms.assetid: 46926379-0561-46bd-a531-04951e65b765
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::GetOriginalValue
Retrieves the initial value of the current property.  
  
## Syntax  
  
```  
const COleVariant& GetOriginalValue() const;  
```  
  
## Return Value  
 The original value of the current property.  
  
## Remarks  
 Use this method to undo the effect of an edit operation that changes the value of the current property.  
  
 The original value of the current property is set by the [CMFCPropertyGridProperty::CMFCPropertyGridProperty](../vs140/CMFCPropertyGridProperty--CMFCPropertyGridProperty.md) constructor, modified by the [CMFCPropertyGridProperty::SetOriginalValue](../vs140/CMFCPropertyGridProperty--SetOriginalValue.md) method, and reset by the [CMFCPropertyGridProperty::ResetOriginalValue](../vs140/CMFCPropertyGridProperty--ResetOriginalValue.md) method.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridProperty::CMFCPropertyGridProperty](../vs140/CMFCPropertyGridProperty--CMFCPropertyGridProperty.md)   
 [CMFCPropertyGridProperty::SetOriginalValue](../vs140/CMFCPropertyGridProperty--SetOriginalValue.md)   
 [CMFCPropertyGridProperty::ResetOriginalValue](../vs140/CMFCPropertyGridProperty--ResetOriginalValue.md)