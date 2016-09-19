---
title: "CUserToolsManager::GetMaxTools"
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
ms.assetid: 6df72bde-6ce4-4c5d-a58f-91102596c0a7
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::GetMaxTools
Returns the maximum number of user tools that can be allocated in the application.  
  
## Syntax  
  
```  
int GetMaxTools() const;  
```  
  
## Return Value  
 The maximum number of user tools that can be allocated.  
  
## Remarks  
 Call this method to retrieve the maximum number of tools that can be allocated in the application. This number is the number of IDs in the range from the `uiCmdFirst` through the `uiCmdLast` parameters that you pass to [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md).  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)