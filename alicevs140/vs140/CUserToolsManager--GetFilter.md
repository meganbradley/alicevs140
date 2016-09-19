---
title: "CUserToolsManager::GetFilter"
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
ms.assetid: 33096b68-8d82-47ed-9022-c79d655130a3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::GetFilter
Returns the file filter that the **File Open** dialog box ([CFileDialog](../vs140/CFileDialog-Class.md)) uses in the **Command** field on the **Tools** tab of the **Customize** dialog box.  
  
## Syntax  
  
```  
const CString& GetFilter() const;  
```  
  
## Return Value  
 A reference to the `CString` object that contains the filter.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)