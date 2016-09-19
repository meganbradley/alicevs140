---
title: "CMFCToolBarButton::SetACCData"
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
ms.assetid: 4f1e8f25-c87b-40e2-a448-0e9f3cb4b554
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::SetACCData
Populates the provided `CAccessibilityData` object with accessibility data from the toolbar button.  
  
## Syntax  
  
```  
virtual BOOL SetACCData(  
   CWnd* pParent,  
   CAccessibilityData& data  
);  
```  
  
#### Parameters  
 [in] `pParent`  
 The parent window of the toolbar button.  
  
 [in] `data`  
 A `CAccessibilityData` object that is populated with the accessibility data of the toolbar button.  
  
## Return Value  
 This method returns `TRUE`.  
  
## Remarks  
 Override this method to return `FALSE` if your toolbar button does not provide accessibility data.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)