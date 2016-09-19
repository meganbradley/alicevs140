---
title: "CMFCRibbonBaseElement::OnProcessKey"
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
ms.assetid: 7521e317-0521-43ef-b91f-b110a7f8d1d1
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::OnProcessKey
Called by the framework when the user presses a shortcut key.  
  
## Syntax  
  
```  
virtual BOOL OnProcessKey(  
   UINT nChar  
);  
```  
  
#### Parameters  
 [in] `nChar`  
 This parameter is not used.  
  
## Return Value  
 Always returns `FALSE`.  
  
## Remarks  
 Override this method if you want the ribbon element to process a shortcut key.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)