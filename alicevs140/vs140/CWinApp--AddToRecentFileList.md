---
title: "CWinApp::AddToRecentFileList"
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
ms.assetid: 772cc033-bb63-4841-b62f-667b9c8559d2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::AddToRecentFileList
Call this member function to add `lpszPathName` to the MRU file list.  
  
## Syntax  
  
```  
  
      virtual void AddToRecentFileList(  
   LPCTSTR lpszPathName   
);  
```  
  
#### Parameters  
 `lpszPathName`  
 The path of the file.  
  
## Remarks  
 You should call the [LoadStdProfileSettings](../vs140/CWinApp--LoadStdProfileSettings.md) member function to load the current MRU file list before you use this member function.  
  
 The framework calls this member function when it opens a file or executes the Save As command to save a file with a new name.  
  
## Example  
 [!CODE [NVC_MFCWindowing#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#36)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::LoadStdProfileSettings](../vs140/CWinApp--LoadStdProfileSettings.md)