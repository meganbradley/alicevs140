---
title: "CEditView::CEditView"
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
ms.assetid: 25431cbe-6756-423c-a3fa-d1fa6c3be531
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::CEditView
Constructs an object of type `CEditView`.  
  
## Syntax  
  
```  
  
CEditView( );  
```  
  
## Remarks  
 After constructing the object, you must call the [CWnd::Create](../vs140/CWnd--Create.md) function before the edit control is used. If you derive a class from `CEditView` and add it to the template using `CWinApp::AddDocTemplate`, the framework calls both this constructor and the **Create** function.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)   
 [CWinApp::AddDocTemplate](../vs140/CWinApp--AddDocTemplate.md)