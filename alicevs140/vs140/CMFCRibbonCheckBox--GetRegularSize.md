---
title: "CMFCRibbonCheckBox::GetRegularSize"
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
ms.assetid: 024a4e2c-be09-4935-a472-58546a87c9e2
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCheckBox::GetRegularSize
Gets the regular size of the checkbox.  
  
## Syntax  
  
```  
virtual CSize GetRegularSize(  
   CDC* pDC  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to the `CDC` object associated with this checkbox.  
  
## Return Value  
 Returns a `CSize` object that contains the regular size of the checkbox.  
  
## Remarks  
 If not overridden, returns the intermediate size of the checkbox.  
  
## Requirements  
 **Header:** afxribboncheckbox.h  
  
## See Also  
 [CMFCRibbonCheckBox Class](../vs140/CMFCRibbonCheckBox-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)