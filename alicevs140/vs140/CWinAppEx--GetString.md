---
title: "CWinAppEx::GetString"
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
ms.assetid: dda5e63f-4da7-4e3f-bc03-b2763d7100a0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetString
Reads string data from a specified registry key.  
  
## Syntax  
  
```  
CString GetString(  
   LPCTSTR lpszEntry,  
   LPCTSTR lpzDefault= _T("")   
);  
```  
  
#### Parameters  
 [in] `lpszEntry`  
 A string that contains the name of a registry key  
  
 [in] `lpzDefault`  
 The default value that the method returns if the specified registry entry does not exist.  
  
## Return Value  
 The string data stored in the registry if successful; `lpszDefault` otherwise.  
  
## Remarks  
 This method reads string data written to the registry. To write data to the registry, use the methods [CWinAppEx::WriteString](../vs140/CWinAppEx--WriteString.md) or [CWinAppEx::WriteSectionString](../vs140/CWinAppEx--WriteSectionString.md).  
  
 The `lpszEntry` parameter is the name of a registry entry located under the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::WriteString](../vs140/CWinAppEx--WriteString.md)   
 [CWinAppEx::WriteSectionString](../vs140/CWinAppEx--WriteSectionString.md)