---
title: "CFrameWnd::m_bAutoMenuEnable"
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
ms.assetid: fb63f177-0fc2-47cd-a264-9e37636df3c8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::m_bAutoMenuEnable
When this data member is enabled (which is the default), menu items that do not have `ON_UPDATE_COMMAND_UI` or `ON_COMMAND` handlers will be automatically disabled when the user pulls down a menu.  
  
## Syntax  
  
```  
  
BOOL m_bAutoMenuEnable;  
  
```  
  
## Remarks  
 Menu items that have an `ON_COMMAND` handler but no `ON_UPDATE_COMMAND_UI` handler will be automatically enabled.  
  
 When this data member is set, menu items are automatically enabled in the same way that toolbar buttons are enabled.  
  
> [!NOTE]
>  `m_bAutoMenuEnable` has no effect on top-level menu items.  
  
 This data member simplifies the implementation of optional commands based on the current selection and reduces the need to write `ON_UPDATE_COMMAND_UI` handlers for enabling and disabling menu items.  
  
## Example  
 [!CODE [NVC_MFCWindowing#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdUI Class](../vs140/CCmdUI-Class.md)   
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)