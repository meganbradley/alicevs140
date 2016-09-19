---
title: "CWinApp::m_pszHelpFilePath"
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
ms.assetid: 75708044-a495-4578-9388-cb3c2e9a4121
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::m_pszHelpFilePath
Contains the path to the application's Help file.  
  
## Syntax  
  
```  
  
LPCTSTR m_pszHelpFilePath;  
  
```  
  
## Remarks  
 By default, the framework initializes `m_pszHelpFilePath` to the name of the application with ".HLP" appended. To change the name of the help file, set `m_pszHelpFilePath` to point to a string that contains the complete name of the desired help file. A convenient place to do this is in the application's [InitInstance](../vs140/CWinApp--InitInstance.md) function. `m_pszHelpFilePath` is a public variable of type **const char\***.  
  
> [!NOTE]
>  If you assign a value to `m_pszHelpFilePath`, it must be dynamically allocated on the heap. The `CWinApp` destructor calls **free**( ) with this pointer. You many want to use the `_tcsdup`( ) run-time library function to do the allocating. Also, free the memory associated with the current pointer before assigning a new value. For example:  
  
 [!CODE [NVC_MFCWindowing#59](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#59)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)