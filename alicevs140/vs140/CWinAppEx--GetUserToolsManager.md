---
title: "CWinAppEx::GetUserToolsManager"
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
ms.assetid: 0b32ffa5-9837-4bc3-b7d4-c94c6b9031ee
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetUserToolsManager
Returns a pointer to the global [CUserToolsManager](../vs140/CUserToolsManager-Class.md) object.  
  
## Syntax  
  
```  
CUserToolsManager* GetUserToolsManager();  
```  
  
## Return Value  
 A pointer to the global `CUserToolsManager` object; `NULL` if user tools management is not enabled for the application.  
  
## Remarks  
 Before you retrieve a pointer to the `CUserToolsManager` object, you must initialize the manager by calling [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md).  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md)