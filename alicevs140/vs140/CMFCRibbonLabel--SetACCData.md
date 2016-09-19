---
title: "CMFCRibbonLabel::SetACCData"
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
ms.assetid: 04f880ca-1dd6-4dd7-a7d2-b04db6a59124
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonLabel::SetACCData
Determines the accessibility data for the current ribbon label element.  
  
## Syntax  
  
```  
virtual BOOL SetACCData(  
    CWnd* pParent,  
    CAccessibilityData& data  
);  
```  
  
#### Parameters  
 [in] `pParent`  
 Represents the parent window of the current ribbon label.  
  
 [out] `data`  
 An object of type `CAccessibilityData` that is populated with the accessibility data of the current ribbon label.  
  
## Return Value  
 `TRUE` if the `data` parameter was successfully populated with the accessibility data of the current ribbon label; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxRibbonLabel.h  
  
## See Also  
 [CMFCRibbonLabel Class](../vs140/CMFCRibbonLabel-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)