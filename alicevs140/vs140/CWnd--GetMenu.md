---
title: "CWnd::GetMenu"
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
ms.assetid: b498b0d5-81f2-472c-8cae-ba263d73ec1e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetMenu
Retrieves a pointer to the menu for this window.  
  
## Syntax  
  
```  
  
CMenu* GetMenu( ) const;  
```  
  
## Return Value  
 Identifies the menu. The value is **NULL** if `CWnd` has no menu. The return value is undefined if `CWnd` is a child window.  
  
 The returned pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 This function should not be used for child windows because they do not have a menu.  
  
## Example  
 [!CODE [NVC_MFCWindowing#98](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#98)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetMenu](http://msdn.microsoft.com/library/windows/desktop/ms647640)