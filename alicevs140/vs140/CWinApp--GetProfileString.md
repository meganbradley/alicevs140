---
title: "CWinApp::GetProfileString"
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
ms.assetid: 69c1cefd-8ee2-436d-90d4-50dc201d04fd
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetProfileString
Call this member function to retrieve the string associated with an entry within the specified section in the application's registry or .INI file.  
  
## Syntax  
  
```  
  
      CString GetProfileString(  
   LPCTSTR lpszSection,  
   LPCTSTR lpszEntry,  
   LPCTSTR lpszDefault = NULL   
);  
```  
  
#### Parameters  
 `lpszSection`  
 Points to a null-terminated string that specifies the section containing the entry.  
  
 `lpszEntry`  
 Points to a null-terminated string that contains the entry whose string is to be retrieved. This value must not be **NULL**.  
  
 `lpszDefault`  
 Points to the default string value for the given entry if the entry cannot be found in the initialization file.  
  
## Return Value  
 The return value is the string from the application's .INI file or `lpszDefault` if the string cannot be found. The maximum string length supported by the framework is `_MAX_PATH`. If `lpszDefault` is **NULL**, the return value is an empty string.  
  
## Remarks  
  
> [!IMPORTANT]
>  The data returned by this function is not necessarily NULL terminated, and the caller must perform validation. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
## Example  
 [!CODE [NVC_MFCWindowing#43](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#43)]  
  
 For another example, see the example for [CWinApp::GetProfileInt](../vs140/CWinApp--GetProfileInt.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::GetProfileInt](../vs140/CWinApp--GetProfileInt.md)   
 [CWinApp::WriteProfileString](../vs140/CWinApp--WriteProfileString.md)   
 [GetPrivateProfileString](http://msdn.microsoft.com/library/windows/desktop/ms724353)