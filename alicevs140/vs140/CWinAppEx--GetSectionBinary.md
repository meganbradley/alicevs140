---
title: "CWinAppEx::GetSectionBinary"
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
ms.assetid: 832cb675-08d0-4a52-8e37-cbcb9d1f2b05
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetSectionBinary
Reads binary data from the registry.  
  
## Syntax  
  
```  
BOOL GetSectionBinary(  
   LPCTSTR lpszSubSection,  
   LPCTSTR lpszEntry,  
   LPBYTE* ppData,  
   UINT* pBytes   
);  
```  
  
#### Parameters  
 [in] `lpszSubSection`  
 A string that contains the relative path of a registry key.  
  
 [in] `lpszEntry`  
 A string that contains the value to read.  
  
 [out] `ppData`  
 A pointer to the buffer where the method stores the data.  
  
 [out] `pBytes`  
 A pointer to an unsigned integer. The method writes the size of `ppData` to this parameter.  
  
## Return Value  
 `True` if successful; otherwise `false`.  
  
## Remarks  
 This method reads binary data that is written to the registry using the methods [CWinAppEx::WriteBinary](../vs140/CWinAppEx--WriteBinary.md) and [CWinAppEx::WriteSectionBinary](../vs140/CWinAppEx--WriteSectionBinary.md).  
  
 The `lpszSubSection` parameter is not an absolute path for a registry entry. It is a relative path that is appended to the end of the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::WriteBinary](../vs140/CWinAppEx--WriteBinary.md)   
 [CWinAppEx::WriteSectionBinary](../vs140/CWinAppEx--WriteSectionBinary.md)   
 [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md)