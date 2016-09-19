---
title: "CUserTool::m_strArguments"
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
ms.assetid: 73f30dc5-b218-4a51-be17-d6b69461743d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserTool::m_strArguments
The command-line arguments for the user tool.  
  
## Syntax  
  
```  
CString m_strArguments;  
```  
  
## Remarks  
 This string is passed to the tool when you call [CUserTool::Invoke](../vs140/CUserTool--Invoke.md) or when a user clicks the command associated with this tool.  
  
## Requirements  
 **Header:** afxusertool.h  
  
## See Also  
 [CUserTool Class](../vs140/CUserTool-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)