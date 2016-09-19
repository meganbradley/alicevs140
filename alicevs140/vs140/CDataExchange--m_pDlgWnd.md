---
title: "CDataExchange::m_pDlgWnd"
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
ms.assetid: 68d2862f-3ffe-464f-9c97-04b408a95cdd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataExchange::m_pDlgWnd
Contains a pointer to the [CWnd](../vs140/CWnd-Class.md) object for which dialog data exchange (DDX) or validation (DDV) is taking place.  
  
## Syntax  
  
```  
  
CWnd* m_pDlgWnd;  
  
```  
  
## Remarks  
 This object is usually a [CDialog](../vs140/CDialog-Class.md) object. Implementors of custom DDX or DDV routines can use this pointer to obtain access to the dialog window that contains the controls they are operating on.  
  
 For more information on writing your own DDX and DDV routines, see [Technical Note 26](../vs140/TN026--DDX-and-DDV-Routines.md). For an overview of DDX and DDV, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md) and [Dialog Box Topics](../vs140/Dialog-Boxes.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDataExchange Class](../vs140/CDataExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)