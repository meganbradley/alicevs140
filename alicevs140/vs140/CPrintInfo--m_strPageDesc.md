---
title: "CPrintInfo::m_strPageDesc"
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
ms.assetid: e469093f-a3f5-4320-9e20-21ec188a7d92
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::m_strPageDesc
Contains a format string used to display the page numbers during print preview; this string consists of two substrings, one for single-page display and one for double-page display, each terminated by a '\n' character.  
  
## Remarks  
 The framework uses "Page %u\nPages %u-%u\n" as the default value. If you want a different format for the page numbers, specify a format string in your override of `CView::OnPreparePrinting`. The **m_strPageDesc** member is a public variable of type `CString`.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md)