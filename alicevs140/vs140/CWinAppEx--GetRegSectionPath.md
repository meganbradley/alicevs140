---
title: "CWinAppEx::GetRegSectionPath"
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
ms.assetid: c7ca78b8-a308-4791-8c5b-a809d74aac7b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetRegSectionPath
Creates and returns the absolute path of a registry key.  
  
## Syntax  
  
```  
CString GetRegSectionPath(  
   LPCTSTR szSectionAdd = _T("")  
);  
```  
  
#### Parameters  
 [in] `szSectionAdd`  
 A string that contains the relative path of a registry key.  
  
## Return Value  
 A `CString` that contains the absolute path of a registry key.  
  
## Remarks  
 This method defines the registry key's absolute path by appending the relative path in `szSectionAdd` to the default registry location for your application. To get the default registry key, use the method [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md).  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md)