---
title: "CWinApp::GetProfileInt"
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
ms.assetid: d3bdb3b1-a7c3-4151-a5b6-45beca2f76e1
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::GetProfileInt
Call this member function to retrieve the value of an integer from an entry within a specified section of the application's registry or .INI file.  
  
## Syntax  
  
```  
  
      UINT GetProfileInt(  
   LPCTSTR lpszSection,  
   LPCTSTR lpszEntry,  
   int nDefault   
);  
```  
  
#### Parameters  
 `lpszSection`  
 Points to a null-terminated string that specifies the section containing the entry.  
  
 `lpszEntry`  
 Points to a null-terminated string that contains the entry whose value is to be retrieved.  
  
 `nDefault`  
 Specifies the default value to return if the framework cannot find the entry.  
  
## Return Value  
 The integer value of the string that follows the specified entry if the function is successful. The return value is the value of the `nDefault` parameter if the function does not find the entry. The return value is 0 if the value that corresponds to the specified entry is not an integer.  
  
 This member function supports hexadecimal notation for the value in the .INI file. When you retrieve a signed integer, you should cast the value into an `int`.  
  
## Remarks  
 This member function is not case sensitive, so the strings in the `lpszSection` and `lpszEntry` parameters may differ in case.  
  
> [!IMPORTANT]
>  The data returned by this function is not necessarily NULL terminated, and the caller must perform validation. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
## Example  
 [!CODE [NVC_MFCWindowing#42](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#42)]  
  
 For an additional example, see [CWinApp::WriteProfileInt](../vs140/CWinApp--WriteProfileInt.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::GetProfileString](../vs140/CWinApp--GetProfileString.md)   
 [CWinApp::WriteProfileInt](../vs140/CWinApp--WriteProfileInt.md)   
 [GetPrivateProfileInt](http://msdn.microsoft.com/library/windows/desktop/ms724345)