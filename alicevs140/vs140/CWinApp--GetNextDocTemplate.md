---
title: "CWinApp::GetNextDocTemplate"
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
ms.assetid: ed60a32e-e37b-4a32-9efa-ce1454876286
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetNextDocTemplate
Gets the document template identified by `pos`, then sets `pos` to the **POSITION** value.  
  
## Syntax  
  
```  
  
      CDocTemplate* GetNextDocTemplate(  
   POSITION& pos   
) const;  
```  
  
#### Parameters  
 `pos`  
 A reference to a **POSITION** value returned by a previous call to `GetNextDocTemplate` or [GetFirstDocTemplatePosition](../vs140/CWinApp--GetFirstDocTemplatePosition.md). The value is updated to the next position by this call.  
  
## Return Value  
 A pointer to a [CDocTemplate](../vs140/CDocTemplate-Class.md) object.  
  
## Remarks  
 You can use `GetNextDocTemplate` in a forward iteration loop if you establish the initial position with a call to `GetFirstDocTemplatePosition`.  
  
 You must ensure that your **POSITION** value is valid. If it is invalid, then the Debug version of the Microsoft Foundation Class Library asserts.  
  
 If the retrieved document template is the last available, then the new value of `pos` is set to **NULL**.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::AddDocTemplate](../vs140/CWinApp--AddDocTemplate.md)