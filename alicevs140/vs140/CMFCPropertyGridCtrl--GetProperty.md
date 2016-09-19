---
title: "CMFCPropertyGridCtrl::GetProperty"
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
ms.assetid: 32101829-548a-4bcb-9da8-80f564f18d5b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::GetProperty
Retrieves a pointer to the property object that corresponds to the specified index of an item in a property grid control.  
  
## Syntax  
  
```  
CMFCPropertyGridProperty* GetProperty(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 [in] `nIndex`  
 The zero-based index of a property grid control item.  
  
 This method asserts if the `nIndex` parameter is less than zero or greater than or equal to the number of properties.  
  
## Return Value  
 A pointer to the property object that corresponds to the specified index if this method is successful; otherwise, `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)