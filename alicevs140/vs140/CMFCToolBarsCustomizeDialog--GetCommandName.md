---
title: "CMFCToolBarsCustomizeDialog::GetCommandName"
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
ms.assetid: da335974-2faf-4e00-8a31-9a68819e59c7
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::GetCommandName
Retrieves the name that is associated with the given command ID.  
  
## Syntax  
  
```  
LPCTSTR GetCommandName(  
   UINT uiCmd  
) const;  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The ID of the command to retrieve.  
  
## Return Value  
 The name that is associated with the given command ID, or `NULL` if the command does not exist.  
  
## Requirements  
 **Header:** afxtoolbarscustomizedialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)