---
title: "Standard Command and Window IDs"
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
ms.topic: article
ms.assetid: 0424805c-fff8-4531-8f0c-15cfb13aa612
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Standard Command and Window IDs
The Microsoft Foundation Class Library defines a number of standard command and window IDs in Afxres.h. These IDs are most commonly used within the resource editors and the Properties window to map messages to your handler functions. All standard commands have an **ID_** prefix. For example, when you use the menu editor, you normally bind the File Open menu item to the standard `ID_FILE_OPEN` command ID.  
  
 For most standard commands, application code does not need to refer to the command ID, because the framework itself handles the commands through message maps in its primary framework classes (`CWinThread`, `CWinApp`, `CView`, **CDocument**, and so on).  
  
 In addition to standard command IDs, a number of other standard IDs are defined which have a prefix of **AFX_ID**. These IDs include standard window IDs (prefix **AFX_IDW_**), string IDs (prefix **AFX_IDS_**), and several other types.  
  
 IDs that begin with the **AFX_ID** prefix are rarely used by programmers, but you might need to refer to these IDs when overriding framework functions that also refer to the **AFX_ID**s.  
  
 IDs are not individually documented in this reference. You can find more information on them in Technical Notes [20](../vs140/TN020--ID-Naming-and-Numbering-Conventions.md), [21](../vs140/TN021--Command-and-Message-Routing.md), and [22](../vs140/TN022--Standard-Commands-Implementation.md).  
  
> [!NOTE]
>  The header file Afxres.h is indirectly included in Afxwin.h. You must explicitly include the following statement in your application's resource script (.rc) file:  
  
 [!CODE [NVC_MFC_Utilities#47](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#47)]  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)