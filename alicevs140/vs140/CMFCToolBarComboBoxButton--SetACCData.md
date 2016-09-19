---
title: "CMFCToolBarComboBoxButton::SetACCData"
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
ms.assetid: e1f2f6fa-b73b-4f34-a3ee-08b6ae4630bb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::SetACCData
Populates the specified `CAccessibilityData` object by using accessibility data from the combo box button.  
  
## Syntax  
  
```  
 virtual BOOL SetACCData(  
   CWnd* pParent,  
   CAccessibilityData& data  
);  
```  
  
#### Parameters  
 [in] `pParent`  
 The parent window of the combo box button.  
  
 [out] `data`  
 A `CAccessibilityData` object that receives the accessibility data from the combo box button.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise `FALSE`.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)