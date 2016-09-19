---
title: "CMFCPropertyGridColorProperty::SetOriginalValue"
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
ms.assetid: 9cda1d8e-e634-48e6-be7a-4be68c916daa
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridColorProperty::SetOriginalValue
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
 [CMFCPropertyGridColorProperty](../vs140/CMFCPropertyGridColorProperty-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridProperty::ResetOriginalValue](../vs140/CMFCPropertyGridProperty--ResetOriginalValue.md)   
 [COleVariant Class](../vs140/COleVariant-Class.md)