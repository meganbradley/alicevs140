---
title: "CStatic::GetCursor"
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
ms.assetid: 72c46838-adf5-43bf-b23f-326b512fb56e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatic::GetCursor
Gets the handle of the cursor, previously set with [SetCursor](../vs140/CStatic--SetCursor.md), that is associated with `CStatic`.  
  
## Syntax  
  
```  
  
HCURSOR GetCursor( );  
  
```  
  
## Return Value  
 A handle to the current cursor, or **NULL** if no cursor has been set.  
  
## Example  
 [!CODE [NVC_MFC_CStatic#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatic#4)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CStatic Class](../vs140/CStatic-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatic::SetCursor](../vs140/CStatic--SetCursor.md)   
 [STM_GETIMAGE](http://msdn.microsoft.com/library/windows/desktop/bb760778)   
 [Cursors](http://msdn.microsoft.com/library/windows/desktop/ms646970)