---
title: "CSettingsStore::Open"
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
ms.assetid: 6836fe81-f4dd-4c12-9905-7fbc0347fe37
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSettingsStore::Open
Opens a registry key.  
  
## Syntax  
  
```  
virtual BOOL Open(  
   LPCTSTR pszPath   
);  
```  
  
#### Parameters  
 [in] `pszPath`  
 The name of a registry key.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 After this method successfully opens the specified key, it sets `m_hKey` to the handle of this key.  
  
## Requirements  
 **Header:** afxsettingsstore.h  
  
## See Also  
 [CSettingsStore Class](../vs140/CSettingsStore-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)