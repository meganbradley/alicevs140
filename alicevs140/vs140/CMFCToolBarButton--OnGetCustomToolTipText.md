---
title: "CMFCToolBarButton::OnGetCustomToolTipText"
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
ms.assetid: 1a3e596e-5ca1-4df2-945c-c7c004d73b37
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::OnGetCustomToolTipText
Called by the framework to retrieve the custom tooltip text for the button.  
  
## Syntax  
  
```  
virtual BOOL OnGetCustomToolTipText(  
   CString& strToolTip  
);  
```  
  
#### Parameters  
 [out] `strToolTip`  
 A `CString` object that receives the custom tooltip text.  
  
## Return Value  
 This method returns `FALSE`.  
  
## Remarks  
 The framework calls this method when it displays the tooltip for the toolbar button. If this method returns `FALSE`, the framework uses a default tooltip.  
  
 The default implementation does nothing and returns `FALSE`. Override this method and return a nonzero value to provide custom tooltip text for the toolbar button.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)