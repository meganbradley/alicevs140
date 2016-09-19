---
title: "CMFCPropertyGridCtrl::EditItem"
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
ms.assetid: d6edf8b8-0405-4083-97c4-1386cbc74b65
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::EditItem
Called by the framework when the user starts to modify a property.  
  
## Syntax  
  
```  
virtual BOOL EditItem(  
   CMFCPropertyGridProperty* pProp,  
   LPPOINT lptClick=NULL   
);  
```  
  
#### Parameters  
 [in] `pProp`  
 Pointer to a property.  
  
 [in] `lptClick`  
 The point on the property grid control that the user clicked to begin the edit operation. The point is in the client coordinates of the control. The default value is `NULL`.  
  
## Return Value  
 `TRUE` if method is successful; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)