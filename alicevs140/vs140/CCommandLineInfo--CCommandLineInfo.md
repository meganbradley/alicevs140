---
title: "CCommandLineInfo::CCommandLineInfo"
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
ms.assetid: 9aba3192-75f5-47b7-9866-bc096a6411ca
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCommandLineInfo::CCommandLineInfo
This constructor creates a `CCommandLineInfo` object with default values.  
  
## Syntax  
  
```  
  
CCommandLineInfo( );  
  
```  
  
## Remarks  
 The default is to show the splash screen (`m_bShowSplash` **= TRUE**) and to execute the New command on the File menu (`m_nShellCommand` **= NewFile**).  
  
 The application framework calls [ParseParam](../vs140/CCommandLineInfo--ParseParam.md) to fill data members of this object.  
  
## Example  
 [!CODE [NVC_MFCDocView#54](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#54)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCommandLineInfo Class](../vs140/CCommandLineInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCommandLineInfo::ParseParam](../vs140/CCommandLineInfo--ParseParam.md)