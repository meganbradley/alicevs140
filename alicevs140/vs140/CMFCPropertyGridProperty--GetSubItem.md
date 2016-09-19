---
title: "CMFCPropertyGridProperty::GetSubItem"
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
ms.assetid: 27fb42e3-ad01-4a90-946e-d07040a61fde
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::GetSubItem
Retrieves a sub-property identified by a zero-based index.  
  
## Syntax  
  
```  
CMFCPropertyGridProperty* GetSubItem(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 [in] `nIndex`  
 The zero-based index of the property to retrieve. This parameter is invalid if it is less than zero or greater than or equal to the number of sub-properties.  
  
## Return Value  
 A pointer to a property object that is a child item of this property.  
  
 -or-  
  
 In retail mode, `NULL` if the `nIndex` parameter is invalid. In debug mode, this method asserts.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)