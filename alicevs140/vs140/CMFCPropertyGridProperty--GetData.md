---
title: "CMFCPropertyGridProperty::GetData"
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
ms.assetid: 84c6d893-132f-46d3-ae7d-ef65312621d5
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::GetData
Retrieves a `DWORD` value that is associated with a property.  
  
## Syntax  
  
```  
DWORD_PTR GetData() const;  
```  
  
## Return Value  
 A `DWORD` value.  
  
## Remarks  
 The data that is returned is an application-specific value, such as a number or a pointer to other data. Specify the data value when you construct the property or when you call the [CMFCPropertyGridProperty::SetData](../vs140/CMFCPropertyGridProperty--SetData.md) method.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridProperty::SetData](../vs140/CMFCPropertyGridProperty--SetData.md)   
 [CMFCPropertyGridProperty::CMFCPropertyGridProperty](../vs140/CMFCPropertyGridProperty--CMFCPropertyGridProperty.md)