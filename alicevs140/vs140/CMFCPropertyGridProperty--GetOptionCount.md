---
title: "CMFCPropertyGridProperty::GetOptionCount"
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
ms.assetid: 7c2f8867-86ca-482c-9ebe-dcf19894cd9a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::GetOptionCount
Retrieves the number of options that belong to a property.  
  
## Syntax  
  
```  
int GetOptionCount() const;  
```  
  
## Return Value  
 The number of property list items (options) that are contained in the property control.  
  
## Remarks  
 Call the [CMFCPropertyGridProperty::AddOption](../vs140/CMFCPropertyGridProperty--AddOption.md) method to add items to the property list. Call the [CMFCPropertyGridProperty::RemoveAllOptions](../vs140/CMFCPropertyGridProperty--RemoveAllOptions.md) method to remove all items.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)