---
title: "CMFCPropertyGridProperty::SetOriginalValue"
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
ms.assetid: 6f5f6e0e-dccc-4d5c-832b-6dd25c8c5f86
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::SetOriginalValue
Sets the original value of an editable property.  
  
## Syntax  
  
```  
virtual void SetOriginalValue(  
   const COleVariant& varValue  
);  
```  
  
#### Parameters  
 [in] `varValue`  
 A value.  
  
## Remarks  
 Use the [CMFCPropertyGridProperty::ResetOriginalValue](../vs140/CMFCPropertyGridProperty--ResetOriginalValue.md) method to reset the original value of an edited property.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridProperty::ResetOriginalValue](../vs140/CMFCPropertyGridProperty--ResetOriginalValue.md)   
 [COleVariant Class](../vs140/COleVariant-Class.md)