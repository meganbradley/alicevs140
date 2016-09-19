---
title: "CMFCPropertySheet::OnRemoveTreePage"
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
ms.assetid: 4625dffa-b84f-410b-914b-22abbc8b3ce5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertySheet::OnRemoveTreePage
Called by the framework to remove a property page from a tree control.  
  
## Syntax  
  
```  
virtual BOOL OnRemoveTreePage(  
   CPropertyPage* pPage   
);  
```  
  
#### Parameters  
 [in] `pPage`  
 Pointer to a property page object that represents the property page to remove.  
  
## Return Value  
 `TRUE` if this method is successful; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxpropertysheet.h  
  
## See Also  
 [CMFCPropertySheet Class](../vs140/CMFCPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)