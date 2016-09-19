---
title: "CPrintDialogEx::PrintRange"
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
ms.assetid: a940734b-bc69-45b6-ada2-f9f172ca7405
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::PrintRange
Call this function after calling `DoModal` to determine whether to print only a range of pages in the document.  
  
## Syntax  
  
```  
  
BOOL PrintRange( ) const;  
  
```  
  
## Return Value  
 **TRUE** if only a range of pages in the document are to be printed; otherwise **FALSE**.  
  
## Remarks  
 The specified page ranges can be determined from [m_pdex](../vs140/CPrintDialogEx--m_pdex.md) (see **nPageRanges**, **nMaxPageRanges**, and **lpPageRanges** in the [PRINTDLGEX](http://msdn.microsoft.com/library/windows/desktop/ms646844) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialogEx::PrintAll](../vs140/CPrintDialogEx--PrintAll.md)   
 [CPrintDialogEx::PrintCurrentPage](../vs140/CPrintDialogEx--PrintCurrentPage.md)   
 [CPrintDialogEx::PrintSelection](../vs140/CPrintDialogEx--PrintSelection.md)