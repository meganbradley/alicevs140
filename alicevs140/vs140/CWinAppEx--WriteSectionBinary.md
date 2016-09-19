---
title: "CWinAppEx::WriteSectionBinary"
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
ms.assetid: c5dc07df-c273-4f22-a36e-e4a1bbbad654
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::WriteSectionBinary
Writes binary data to a value in the registry.  
  
## Syntax  
  
```  
BOOL WriteSectionBinary(  
   LPCTSTR lpszSubSection,  
   LPCTSTR lpszEntry,  
   LPBYTE pData,  
   UINT nBytes   
);  
```  
  
#### Parameters  
 [in] `lpszSubSection`  
 A string that contains the name of a registry key  
  
 [in] `lpszEntry`  
 A string that contains the value to set.  
  
 [in] `pData`  
 The data to write to the registry.  
  
 [in] `nBytes`  
 The size of `pData` in bytes.  
  
## Return Value  
 `TRUE` if this method is successful; otherwise `FALSE`.  
  
## Remarks  
 The `lpszSubSection` parameter is not the absolute path for a registry entry. It is a relative path that is appended to the end of the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
 If the key specified by `lpszEntry` does not exist, this method will create it.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)