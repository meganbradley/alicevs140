---
title: "CMFCRibbonPanel::IsMainPanel"
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
ms.assetid: 7419dbf4-c1ab-4603-b1ec-9719820edfe4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonPanel::IsMainPanel
Indicates whether the ribbon panel is the main ribbon panel.  
  
## Syntax  
  
```  
virtual BOOL IsMainPanel() const;  
```  
  
## Return Value  
 Always returns `FALSE`.  
  
## Remarks  
 This method always returns `FALSE`. Override this method to indicate whether the ribbon panel is the main ribbon panel.  
  
 The main ribbon panel is displayed when the user selects the application button.  
  
## Requirements  
 **Header:** afxribbonpanel.h  
  
## See Also  
 [CMFCRibbonPanel Class](../vs140/CMFCRibbonPanel-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)