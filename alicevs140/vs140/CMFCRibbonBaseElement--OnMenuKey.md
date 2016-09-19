---
title: "CMFCRibbonBaseElement::OnMenuKey"
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
ms.assetid: 56dbca81-3326-4537-bce1-91daba2ebcc3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::OnMenuKey
Called by the framework when the user presses a menu keytip on the main panel.  
  
## Syntax  
  
```  
virtual BOOL OnMenuKey(  
    UINT nUpperChar  
);  
```  
  
#### Parameters  
 [in] `nUpperChar`  
 This parameter is not used.  
  
## Return Value  
 Always returns `FALSE`.  
  
## Remarks  
 By default this method always returns `FALSE`. Override this method to respond when a user presses a menu keytip on the main panel.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)