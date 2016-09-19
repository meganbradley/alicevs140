---
title: "CMFCRibbonComboBox::GetIntermediateSize"
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
ms.assetid: 9d71f37b-6992-4207-926c-2e05b22d8f29
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonComboBox::GetIntermediateSize
Returns the size of the combo box as displayed in intermediate mode.  
  
## Syntax  
  
```  
virtual CSize GetIntermediateSize(  
   CDC* pDC  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context for the combo box.  
  
## Return Value  
 The size of the combo box.  
  
## Remarks  
 The size returned is based on the size of the combo box when it displays small images.  
  
## Requirements  
 **Header:** afxribboncombobox.h  
  
## See Also  
 [CMFCRibbonComboBox Class](../vs140/CMFCRibbonComboBox-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)