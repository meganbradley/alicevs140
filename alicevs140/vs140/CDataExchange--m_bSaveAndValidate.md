---
title: "CDataExchange::m_bSaveAndValidate"
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
ms.assetid: 3565c583-ba9d-467c-99ca-03c544fa5c7a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataExchange::m_bSaveAndValidate
This flag indicates the direction of a dialog data exchange (DDX) operation.  
  
## Syntax  
  
```  
  
BOOL m_bSaveAndValidate;  
  
```  
  
## Remarks  
 The flag is nonzero if the `CDataExchange` object is being used to move data from the dialog controls to dialog-class data members after the user edits the controls. The flag is zero if the object is being used to initialize dialog controls from dialog-class data members.  
  
 The flag is also nonzero during dialog data validation (DDV).  
  
 For more information on writing your own DDX and DDV routines, see [Technical Note 26](../vs140/TN026--DDX-and-DDV-Routines.md). For an overview of DDX and DDV, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md) and [Dialog Box Topics](../vs140/Dialog-Boxes.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDataExchange Class](../vs140/CDataExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)