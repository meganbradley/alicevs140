---
title: "CWinAppEx::WriteObject"
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
ms.assetid: 525a9ce5-85a6-43ea-9ae4-e121456054b9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::WriteObject
Writes data derived from the [CObject Class](../vs140/CObject-Class.md) to the registry.  
  
## Syntax  
  
```  
BOOL WriteObject(  
   LPCTSTR lpszEntry,  
   CObject& obj   
);  
```  
  
#### Parameters  
 [in] `lpszEntry`  
 A string that contains the value to set.  
  
 [in] `obj`  
 A reference to `CObject` data that the method will store.  
  
## Return Value  
 `TRUE` if this method is successful; otherwise `FALSE`.  
  
## Remarks  
 This method writes the `obj` data to the specified value under the default registry key. Use [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) to determine the current registry key.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)