---
title: "CUserTool::SetToolIcon"
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
ms.assetid: 0d1285f8-1efe-4d1f-b7bc-fcfed25f137c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserTool::SetToolIcon
Loads the icon for the user tool from the application that the tool uses.  
  
## Syntax  
  
```  
virtual HICON SetToolIcon();  
```  
  
## Return Value  
 A handle to the loaded icon.  
  
## Remarks  
 Call this method to load the icon to be displayed on the menu item. This method searches for the icon in the executable file that the tool uses. If it does not have a default icon, the icon provided by [CUserTool::LoadDefaultIcon](../vs140/CUserTool--LoadDefaultIcon.md) is used instead.  
  
## Requirements  
 **Header:** afxusertool.h  
  
## See Also  
 [CUserTool Class](../vs140/CUserTool-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)