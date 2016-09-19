---
title: "CSettingsStore::DeleteValue"
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
ms.assetid: 6aba7f4c-9630-4e34-909b-3ff4eee72eba
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSettingsStore::DeleteValue
Deletes a value from `m_hKey`.  
  
## Syntax  
  
```  
virtual BOOL DeleteValue(  
   LPCTSTR pszValue   
);  
```  
  
#### Parameters  
 [in] `pszValue`  
 Specifies the value field to remove.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxsettingsstore.h  
  
## See Also  
 [CSettingsStore Class](../vs140/CSettingsStore-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)