---
title: "CUserToolsManager::GetUserTools"
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
ms.assetid: 7c607435-02e9-4562-a983-dd00e04b4081
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::GetUserTools
Returns a reference to the list of user tools.  
  
## Syntax  
  
```  
const CObList& GetUserTools() const;  
```  
  
## Return Value  
 A const reference to a [CObList](../vs140/CObList-Class.md) object that contains a list of user tools.  
  
## Remarks  
 Call this method to retrieve a list of user tools that the [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md) object maintains. Each user tool is represented by an object of type [CUserTool Class](../vs140/CUserTool-Class.md) or a type derived from `CUserTool`. The type is specified by the `pToolRTC` parameter when you call [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md) to enable user tools.  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)