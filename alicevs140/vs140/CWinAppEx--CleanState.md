---
title: "CWinAppEx::CleanState"
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
ms.assetid: 01c45cf9-91bd-4fae-ac68-2559d91e8c09
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::CleanState
Removes all the information about the application from the Windows registry.  
  
## Syntax  
  
```  
virtual BOOL CleanState(  
   LPCTSTR lpszSectionName=NULL   
);  
```  
  
#### Parameters  
 [in] `lpszSectionName`  
 A string that contains a path of a registry key.  
  
## Return Value  
 Nonzero if the method was successful; otherwise 0.  
  
## Remarks  
 This method clears application data from a specific section of the registry. You can specify the section to clear by using the parameter `lpszSectionName`. If `lpszSectionName` is `NULL`, this method will use the default registry path stored in the `CWinAppEx` object. To get the default registry path, use [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md).  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md)