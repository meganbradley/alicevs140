---
title: "CUserTool::SetCommand"
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
ms.assetid: 33179cdb-1e40-4dd8-ace1-2ce9c3b57d2d
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserTool::SetCommand
Sets the application that the user tool runs.  
  
## Syntax  
  
```  
void SetCommand(  
   LPCTSTR lpszCmd   
);  
```  
  
#### Parameters  
 [in] `lpszCmd`  
 Specifies the new application to be associated with the user tool.  
  
## Remarks  
 Call this method to set a new application that the user tool runs. The method destroys the old icon and loads a new icon from the given application. If it cannot load an icon from the application, it loads the default icon for a user tool by calling [CUserTool::LoadDefaultIcon](../vs140/CUserTool--LoadDefaultIcon.md).  
  
## Requirements  
 **Header:** afxusertool.h  
  
## See Also  
 [CUserTool Class](../vs140/CUserTool-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)