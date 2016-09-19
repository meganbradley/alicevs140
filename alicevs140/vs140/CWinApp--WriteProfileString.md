---
title: "CWinApp::WriteProfileString"
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
ms.assetid: e4ec9194-5f7a-480e-856c-b9ccfa782039
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::WriteProfileString
Call this member function to write the specified string into the specified section of the application's registry or .INI file.  
  
## Syntax  
  
```  
  
      BOOL WriteProfileString(  
   LPCTSTR lpszSection,  
   LPCTSTR lpszEntry,  
   LPCTSTR lpszValue   
);  
```  
  
#### Parameters  
 `lpszSection`  
 Points to a null-terminated string that specifies the section containing the entry. If the section does not exist, it is created. The name of the section is case independent; the string may be any combination of uppercase and lowercase letters.  
  
 `lpszEntry`  
 Points to a null-terminated string that contains the entry into which the value is to be written. If the entry does not exist in the specified section, it is created. If this parameter is `NULL`, the section specified by `lpszSection` is deleted.  
  
 `lpszValue`  
 Points to the string to be written. If this parameter is `NULL`, the entry specified by the `lpszEntry` parameter is deleted.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCWindowing#43](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#43)]  
  
 For another example, see the example for [CWinApp::GetProfileInt](../vs140/CWinApp--GetProfileInt.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::GetProfileString](../vs140/CWinApp--GetProfileString.md)   
 [CWinApp::WriteProfileInt](../vs140/CWinApp--WriteProfileInt.md)   
 [WritePrivateProfileString](http://msdn.microsoft.com/library/windows/desktop/ms725501)   
 [CWinApp::SetRegistryKey](../vs140/CWinApp--SetRegistryKey.md)