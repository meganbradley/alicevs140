---
title: "CWinAppEx::GetSectionString"
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
ms.assetid: 7be6da81-f7e1-42d3-9688-a30deccbbcf3
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetSectionString
Reads string data from the registry.  
  
## Syntax  
  
```  
CString GetSectionString(  
   LPCTSTR lpszSubSection,  
   LPCTSTR lpszEntry,  
   LPCTSTR lpszDefault = _T("")  
);  
```  
  
#### Parameters  
 [in] `lpszSubSection`  
 A string that contains the relative path of a registry key.  
  
 [in] `lpszEntry`  
 A string that contains the value to read.  
  
 [in] `lpszDefault`  
 The default value to return if the specified value does not exist.  
  
## Return Value  
 The string data stored in the specified registry value if the data exists; otherwise `lpszDefault`.  
  
## Remarks  
 This method reads string data written to the registry. Use [CWinAppEx::WriteString](../vs140/CWinAppEx--WriteString.md) and [CWinAppEx::WriteSectionString](../vs140/CWinAppEx--WriteSectionString.md) to write string data to the registry.  
  
 The `lpszSubSection` parameter is not an absolute path for a registry entry. It is a relative path that is appended to the end of the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)