---
title: "CWinAppEx::GetObject"
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
ms.assetid: d31358f4-a665-47f5-914a-26f389314720
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetObject
Reads [CObject](../vs140/CObject-Class.md)-dervied data from the registry.  
  
## Syntax  
  
```  
BOOL GetObject(  
   LPCTSTR lpszEntry,  
   CObject& obj   
);  
```  
  
#### Parameters  
 [in] `lpszEntry`  
 A string that contains the relative path of a registry entry.  
  
 [out] `obj`  
 A reference to a `CObject`. The method uses this reference to store the registry data.  
  
## Return Value  
 Nonzero if the method was successful; otherwise 0.  
  
## Remarks  
 This method reads data from the registry that is derived from `CObject`. To write `CObject` data to the registry, use either [CWinAppEx::WriteObject](../vs140/CWinAppEx--WriteObject.md) or [CWinAppEx::WriteSectionObject](../vs140/CWinAppEx--WriteSectionObject.md).  
  
 The `lpszEntry` parameter is the name of a registry entry that is located under the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::WriteObject](../vs140/CWinAppEx--WriteObject.md)   
 [CWinAppEx::WriteSectionObject](../vs140/CWinAppEx--WriteSectionObject.md)