---
title: "CMFCRibbonEdit::SetACCData"
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
ms.assetid: f57786d2-fb74-46dd-8683-8c00289681b6
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::SetACCData
Sets the accessibility data for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) object.  
  
## Syntax  
  
```  
 virtual BOOL SetACCData(  
   CWnd* pParent,  
   CAccessibilityData& data  
);  
```  
  
#### Parameters  
 `pParent`  
 Pointer to the parent window for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) object.  
  
 `data`  
 The accessibility data for the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) object.  
  
## Return Value  
 Always returns `TRUE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonedit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)