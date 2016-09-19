---
title: "CWinApp::DoMessageBox"
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
ms.assetid: ef07f405-632c-4283-a448-c40e2b96d74c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::DoMessageBox
The framework calls this member function to implement a message box for the global function [AfxMessageBox](../vs140/AfxMessageBox.md).  
  
## Syntax  
  
```  
  
      virtual int DoMessageBox(  
   LPCTSTR lpszPrompt,  
   UINT nType,  
   UINT nIDPrompt   
);  
```  
  
#### Parameters  
 *lpszPrompt*  
 Address of text in the message box.  
  
 `nType`  
 The message box [style](../vs140/Message-Box-Styles.md).  
  
 `nIDPrompt`  
 An index to a Help context string.  
  
## Return Value  
 Returns the same values as `AfxMessageBox`.  
  
## Remarks  
 Do not call this member function to open a message box; use `AfxMessageBox` instead.  
  
 Override this member function to customize your application-wide processing of `AfxMessageBox` calls.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [AfxMessageBox](../vs140/AfxMessageBox.md)   
 [MessageBox](http://msdn.microsoft.com/library/windows/desktop/ms645505)