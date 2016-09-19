---
title: "CWinApp::OnFileOpen"
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
ms.assetid: eb02fa35-0c0a-40e0-92c9-396706d76cb4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::OnFileOpen
Implements the `ID_FILE_OPEN` command.  
  
## Syntax  
  
```  
  
afx_msg void OnFileOpen( );  
```  
  
## Remarks  
 You must add an `ON_COMMAND( ID_FILE_OPEN, OnFileOpen )` statement to your `CWinApp` class message map to enable this member function. If enabled, this function handles execution of the File Open command.  
  
 For information on default behavior and guidance on how to override this member function, see [Technical Note 22](../vs140/TN022--Standard-Commands-Implementation.md).  
  
## Example  
 [!CODE [NVC_MFCWindowing#49](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#49)]  
  
 [!CODE [NVC_MFCWindowing#50](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#50)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnFileNew](../vs140/CWinApp--OnFileNew.md)