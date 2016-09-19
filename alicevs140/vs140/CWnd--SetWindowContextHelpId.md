---
title: "CWnd::SetWindowContextHelpId"
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
ms.assetid: b7617f56-b5f5-4ca2-9629-0bf93cd17284
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetWindowContextHelpId
Call this member function to associate a help context identifier with the specified window.  
  
## Syntax  
  
```  
  
      BOOL SetWindowContextHelpId(  
   DWORD dwContextHelpId   
);  
```  
  
#### Parameters  
 `dwContextHelpId`  
 The help context identifier.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 If a child window does not have a help context identifier, it inherits the identifier of its parent window. Likewise, if an owned window does not have a help context identifier, it inherits the identifier of its owner window. This inheritance of help context identifiers allows an application to set just one identifier for a dialog box and all of its controls.  
  
## Example  
 [!CODE [NVC_MFCWindowing#119](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#119)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetWindowContextHelpId](../vs140/CWnd--GetWindowContextHelpId.md)