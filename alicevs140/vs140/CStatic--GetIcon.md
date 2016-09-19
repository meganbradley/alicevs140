---
title: "CStatic::GetIcon"
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
ms.assetid: 04ab70ce-ccc1-4418-b047-c109fa6442e1
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatic::GetIcon
Gets the handle of the icon, previously set with [SetIcon](../vs140/CStatic--SetIcon.md), that is associated with `CStatic`.  
  
## Syntax  
  
```  
  
HICON GetIcon( ) const;  
```  
  
## Return Value  
 A handle to the current icon, or **NULL** if no icon has been set.  
  
## Example  
 [!CODE [NVC_MFC_CStatic#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatic#6)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CStatic Class](../vs140/CStatic-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatic::SetIcon](../vs140/CStatic--SetIcon.md)   
 [STM_GETICON](http://msdn.microsoft.com/library/windows/desktop/bb760775)   
 [Icons](http://msdn.microsoft.com/library/windows/desktop/ms646973)