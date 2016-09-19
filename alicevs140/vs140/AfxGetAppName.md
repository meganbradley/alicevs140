---
title: "AfxGetAppName"
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
ms.topic: article
ms.assetid: 970fa683-4af6-4107-92e0-e460c9eb823c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetAppName
The string returned by this function can be used for diagnostic messages or as a root for temporary string names.  
  
## Syntax  
  
```  
  
LPCTSTR AFXAPI AfxGetAppName( );   
```  
  
## Return Value  
 A null-terminated string containing the application's name.  
  
## Example  
 [!CODE [NVC_MFCWindowing#127](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#127)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)