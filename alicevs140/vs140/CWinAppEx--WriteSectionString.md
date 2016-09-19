---
title: "CWinAppEx::WriteSectionString"
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
ms.assetid: 6cb5d442-81f2-4031-aaec-fae00ad62f8b
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::WriteSectionString
Writes string data to a value in the registry.  
  
## Syntax  
  
```  
BOOL WriteSectionString(  
   LPCTSTR lpszSubSection,  
   LPCTSTR lpszEntry,  
   LPCTSTR lpszValue   
);  
```  
  
#### Parameters  
 [in] `lpszSubSection`  
 A string that contains the name of a registry key.  
  
 [in] `lpszEntry`  
 A string that contains the value to set.  
  
 [in] `lpszValue`  
 The string data to write to the registry.  
  
## Return Value  
 `TRUE` if this method is successful; otherwise `FALSE`.  
  
## Remarks  
 The `lpszSubSection` parameter is not an absolute path for a registry entry. It is a relative path that is appended to the end of the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md), respectively.  
  
 If the value specified by `lpszEntry` does not exist under `lpszSubSection`, this method will create it.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)