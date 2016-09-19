---
title: "CMFCRibbonCheckBox::SetACCData"
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
ms.assetid: 903b2d1a-346f-40af-80ef-7a9ecb0db9e0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCheckBox::SetACCData
Sets the accessibility data for the checkbox.  
  
## Syntax  
  
```  
virtual BOOL SetACCData(  
   CWnd* pParent,  
   CAccessibilityData& data  
);  
```  
  
#### Parameters  
 `pParent`  
 The parent window of the checkbox.  
  
 `data`  
 The accessibility data for the checkbox.  
  
## Return Value  
 Always returns `TRUE`.  
  
## Remarks  
 By default this method sets the accessibility data for the checkbox and always returns `TRUE`. Override this method to set the accessibility data and return a value that indicates success or failure.  
  
## Requirements  
 **Header:**  
  
## See Also  
 [CMFCRibbonCheckBox Class](../vs140/CMFCRibbonCheckBox-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)