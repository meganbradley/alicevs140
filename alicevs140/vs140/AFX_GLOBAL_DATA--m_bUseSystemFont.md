---
title: "AFX_GLOBAL_DATA::m_bUseSystemFont"
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
ms.topic: article
ms.assetid: 8d24797a-8027-4a6f-94d5-0fcc72a5a4a7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::m_bUseSystemFont
Indicates whether a system font is used for menus, toolbars, and ribbons.  
  
## Syntax  
  
```  
BOOL m_bUseSystemFont;  
```  
  
## Remarks  
 `TRUE` specifies to use a system font; otherwise, `FALSE`. The `AFX_GLOBAL_DATA::AFX_GLOBAL_DATA` constructor initializes this member to `FALSE`.  
  
 Testing this member is not the only way for the framework to determine the font to use. The `AFX_GLOBAL_DATA::UpdateFonts` method also tests default and alternative fonts to determine what visual styles are available to be applied to menus, toolbars, and ribbons.  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)