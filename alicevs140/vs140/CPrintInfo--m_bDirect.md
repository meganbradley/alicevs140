---
title: "CPrintInfo::m_bDirect"
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
ms.assetid: ee103d88-d5d7-42f1-a275-e35d1397f1c3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::m_bDirect
The framework sets this member to **TRUE** if the Print dialog box will be bypassed for direct printing; **FALSE** otherwise.  
  
## Remarks  
 The Print dialog is normally bypassed when you print from the shell or when printing is done using the command ID **ID_FILE_PRINT_DIRECT**.  
  
 You normally don't change this member, but if you do change it, change it before you call [CView::DoPreparePrinting](../vs140/CView--DoPreparePrinting.md) in your override of [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::DoPreparePrinting](../vs140/CView--DoPreparePrinting.md)   
 [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md)