---
title: "CPrintDialogEx::m_pdex"
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
ms.assetid: 5714899b-038c-4909-91e7-06a4a5c7be49
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialogEx::m_pdex
A PRINTDLGEX structure whose members store the characteristics of the dialog object.  
  
## Syntax  
  
```  
  
PRINTDLGEX m_pdex;  
  
```  
  
## Remarks  
 After constructing a `CPrintDialogEx` object, you can use `m_pdex` to set various aspects of the dialog box before calling the [DoModal](../vs140/CPrintDialogEx--DoModal.md) member function. For more information on the `m_pdex` structure, see [PRINTDLGEX](http://msdn.microsoft.com/library/windows/desktop/ms646844) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 If you modify the `m_pdex` data member directly, you will override any default behavior.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialogEx Class](../vs140/CPrintDialogEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)