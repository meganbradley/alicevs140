---
title: "CWinApp::AddDocTemplate"
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
ms.assetid: 9bc1fc63-1cff-4301-b8e9-c4bdda3c8fea
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::AddDocTemplate
Call this member function to add a document template to the list of available document templates that the application maintains.  
  
## Syntax  
  
```  
  
      void AddDocTemplate(  
   CDocTemplate* pTemplate   
);  
```  
  
#### Parameters  
 `pTemplate`  
 A pointer to the `CDocTemplate` to be added.  
  
## Remarks  
 You should add all document templates to an application before you call [RegisterShellFileTypes](../vs140/CWinApp--RegisterShellFileTypes.md).  
  
## Example  
 [!CODE [NVC_MFCWindowing#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#35)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::RegisterShellFileTypes](../vs140/CWinApp--RegisterShellFileTypes.md)   
 [CMultiDocTemplate Class](../vs140/CMultiDocTemplate-Class.md)   
 [CSingleDocTemplate Class](../vs140/CSingleDocTemplate-Class.md)