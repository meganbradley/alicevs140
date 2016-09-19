---
title: "CWinApp::GetFirstDocTemplatePosition"
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
ms.assetid: c732674b-780f-499a-945d-7ff495cf6626
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetFirstDocTemplatePosition
Gets the position of the first document template in the application.  
  
## Syntax  
  
```  
  
POSITION GetFirstDocTemplatePosition( ) const;  
  
```  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if the list is empty.  
  
## Remarks  
 Use the **POSITION** value returned in a call to [GetNextDocTemplate](../vs140/CWinApp--GetNextDocTemplate.md) to get the first [CDocTemplate](../vs140/CDocTemplate-Class.md) object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::AddDocTemplate](../vs140/CWinApp--AddDocTemplate.md)   
 [CWinApp::GetNextDocTemplate](../vs140/CWinApp--GetNextDocTemplate.md)