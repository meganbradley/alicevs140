---
title: "CPrintInfo::m_bPreview"
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
ms.assetid: 593a86eb-170e-4bb6-8e3d-7b08093174df
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::m_bPreview
Contains a flag indicating whether the document is being previewed.  
  
## Remarks  
 This is set by the framework depending on which command the user executed. The Print dialog box is not displayed for a print-preview job. The **m_bPreview** member is a public variable of type **BOOL**.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::DoPreparePrinting](../vs140/CView--DoPreparePrinting.md)   
 [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md)