---
title: "CUserToolsManager::GetInitialDirMenuID"
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
ms.assetid: 3bd686af-630c-4a4c-a75b-7f7c50200d4e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUserToolsManager::GetInitialDirMenuID
Returns the resource ID that is associated with the **Initial directory** menu on the **Tools** tab of the **Customize** dialog box.  
  
## Syntax  
  
```  
UINT GetInitialDirMenuID() const;  
```  
  
## Return Value  
 A menu resource identifier.  
  
## Remarks  
 The returned ID is specified in the `uInitDirMenuID` parameter of [CWinAppEx::EnableUserTools](../vs140/CWinAppEx--EnableUserTools.md).  
  
## Requirements  
 **Header:** afxusertoolsmanager.h  
  
## See Also  
 [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)