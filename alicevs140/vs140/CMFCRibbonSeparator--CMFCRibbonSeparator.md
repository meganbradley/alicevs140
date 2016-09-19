---
title: "CMFCRibbonSeparator::CMFCRibbonSeparator"
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
ms.assetid: 3cfaeeaf-d405-4653-a110-755a5e531f29
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonSeparator::CMFCRibbonSeparator
Constructs a `CMFCRibbonSeparator` object.  
  
## Syntax  
  
```  
CMFCRibbonSeparator(  
   BOOL bIsHoriz = FALSE  
);  
```  
  
#### Parameters  
 [in] `bIsHoriz`  
 If `TRUE`, the separator is horizontal; if `FALSE`, the separator is vertical.  
  
## Remarks  
 Horizontal separators are used in application menus. Vertical separators are used in toolbars.  
  
## Example  
 The following example demonstrates how to construct an object of the `CMFCRibbonSeparator` class.  
  
 [!CODE [NVC_MFC_RibbonApp#19](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#19)]  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonSeparator Class](../vs140/CMFCRibbonSeparator-Class.md)