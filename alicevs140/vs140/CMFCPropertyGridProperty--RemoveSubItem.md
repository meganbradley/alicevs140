---
title: "CMFCPropertyGridProperty::RemoveSubItem"
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
ms.assetid: ee15b15a-6a05-4b84-85ec-5e178252d300
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridProperty::RemoveSubItem
Removes the specified sub-item.  
  
## Syntax  
  
```  
BOOL RemoveSubItem(  
   CMFCPropertyGridProperty*& pProp,  
   BOOL bDelete=TRUE   
);  
```  
  
#### Parameters  
 [in] `pProp`  
 Pointer to a property sub-item.  
  
 [in] `bDelete`  
 `TRUE` to delete the property object that is specified by the `pProp` parameter; otherwise, `FALSE`. The default value is `TRUE`.  
  
## Return Value  
  
## Remarks  
 Specify `FALSE` for the `bDelete` parameter if you intend to move the specified sub-item; that is, remove the sub-item and then add it elsewhere.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridProperty Class](../vs140/CMFCPropertyGridProperty-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)