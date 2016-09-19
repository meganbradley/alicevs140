---
title: "CWinApp::WriteProfileInt"
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
ms.assetid: dc547ec6-242e-47b4-87de-318d1da9bf46
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::WriteProfileInt
Call this member function to write the specified value into the specified section of the application's registry or .INI file.  
  
## Syntax  
  
```  
  
      BOOL WriteProfileInt(  
   LPCTSTR lpszSection,  
   LPCTSTR lpszEntry,  
   int nValue   
);  
```  
  
#### Parameters  
 `lpszSection`  
 Points to a null-terminated string that specifies the section containing the entry. If the section does not exist, it is created. The name of the section is case independent; the string may be any combination of uppercase and lowercase letters.  
  
 `lpszEntry`  
 Points to a null-terminated string that contains the entry into which the value is to be written. If the entry does not exist in the specified section, it is created.  
  
 `nValue`  
 Contains the value to be written.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 This example uses `CWinApp* pApp = AfxGetApp();` to get at the CWinApp class illustrating a way that `WriteProfileString`, `WriteProfileInt`, `GetProfileString`, and `GetProfileInt` can be used from any function in an MFC application.  
  
 [!CODE [NVC_MFCWindowing#43](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#43)]  
  
 For another example, see the example for [CWinApp::GetProfileInt](../vs140/CWinApp--GetProfileInt.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::GetProfileInt](../vs140/CWinApp--GetProfileInt.md)   
 [CWinApp::WriteProfileString](../vs140/CWinApp--WriteProfileString.md)   
 [CWinApp::SetRegistryKey](../vs140/CWinApp--SetRegistryKey.md)