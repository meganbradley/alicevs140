---
title: "CWinAppEx::GetBinary"
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
ms.assetid: 32ae26a8-9347-4f0e-8bee-937738fb6147
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetBinary
Reads binary data from a specified registry key.  
  
## Syntax  
  
```  
BOOL GetBinary(  
   LPCTSTR lpszEntry,  
   LPBYTE* ppData,  
   UINT* pBytes   
);  
```  
  
#### Parameters  
 [in] `lpszEntry`  
 A string that contains the name of a registry key.  
  
 [out] `ppData`  
 A pointer to the buffer that the method fills with the binary data.  
  
 [out] `pBytes`  
 A pointer to an unsigned integer that the method uses to write the number of bytes read.  
  
## Return Value  
 `True` if successful; `false` otherwise.  
  
## Remarks  
 This method reads binary data written to the registry. To write data to the registry, use the methods [CWinAppEx::WriteBinary](../vs140/CWinAppEx--WriteBinary.md) and [CWinAppEx::WriteSectionBinary](../vs140/CWinAppEx--WriteSectionBinary.md).  
  
 The `lpszEntry` parameter is the name of a registry entry located under the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::WriteBinary](../vs140/CWinAppEx--WriteBinary.md)   
 [CWinAppEx::WriteSectionBinary](../vs140/CWinAppEx--WriteSectionBinary.md)