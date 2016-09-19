---
title: "CMFCPropertyGridProperty::SetName"
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
ms.assetid: 4f535aaa-f3dc-4cab-971d-8e713a827243
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::SetName
Sets the name of a property.  
  
## Syntax  
  
```  
void SetName(  
   LPCTSTR lpszName,  
   BOOL bRedraw=TRUE   
);  
```  
  
#### Parameters  
 [in] `lpszName`  
 The property name.  
  
 [in] `bRedraw`  
 `TRUE` to redraw the property immediately; otherwise, `FALSE`. The default value is `TRUE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridProperty::GetName](../vs140/CMFCPropertyGridProperty--GetName.md)