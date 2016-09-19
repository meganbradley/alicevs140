---
title: "CMFCRibbonCheckBox::GetIntermediateSize"
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
ms.assetid: fe2db80d-c1e7-4e83-9917-49f808ae20db
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCheckBox::GetIntermediateSize
Gets the intermediate size of the checkbox.  
  
## Syntax  
  
```  
virtual CSize GetIntermediateSize(  
   CDC* pDC  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to the `CDC` associated with this checkbox.  
  
## Return Value  
 A `CSize` object containing the intermediate size of the checkbox.  
  
## Remarks  
 If not overridden, calculates the intermediate size as the default checkbox size (`AFX_CHECK_BOX_DEFAULT_SIZE`) plus the text size, plus margins.  
  
## Requirements  
 **Header:** afxribboncheckbox.h  
  
## See Also  
 [CMFCRibbonCheckBox Class](../vs140/CMFCRibbonCheckBox-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)