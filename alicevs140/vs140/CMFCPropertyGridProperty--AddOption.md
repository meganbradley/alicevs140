---
title: "CMFCPropertyGridProperty::AddOption"
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
ms.assetid: 434be473-52f8-4ed5-bc4d-209316ac57d8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::AddOption
Adds a new list item to a property list control.  
  
## Syntax  
  
```  
BOOL AddOption(  
   LPCTSTR lpszOption,  
   BOOL bInsertUnique=TRUE   
);  
```  
  
#### Parameters  
 [in] `lpszOption`  
 The list item (option) to add.  
  
 [in] `bInsertUnique`  
 `TRUE` to add the list item only if it does not already exist; otherwise, `FALSE`. The default value is `TRUE`.  
  
## Return Value  
 `TRUE`, which means that the list item is added. Otherwise, `FALSE`, which means that the list item is not added because the `bInsertUnique` parameter is `TRUE` and the list item specified by the `lpszOption` parameter already exists.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)