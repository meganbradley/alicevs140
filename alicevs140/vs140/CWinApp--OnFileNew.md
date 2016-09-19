---
title: "CWinApp::OnFileNew"
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
ms.assetid: ddf79290-2ef7-4715-a1b9-256d3a52e741
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::OnFileNew
Implements the `ID_FILE_NEW` command.  
  
## Syntax  
  
```  
  
afx_msg void OnFileNew( );  
```  
  
## Remarks  
 You must add an `ON_COMMAND( ID_FILE_NEW, OnFileNew )` statement to your `CWinApp` class message map to enable this member function. If enabled, this function handles execution of the File New command.  
  
 See [Technical Note 22](../vs140/TN022--Standard-Commands-Implementation.md) for information on default behavior and guidance on how to override this member function.  
  
## Example  
 [!CODE [NVC_MFCWindowing#49](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#49)]  
  
 [!CODE [NVC_MFCWindowing#50](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#50)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnFileOpen](../vs140/CWinApp--OnFileOpen.md)