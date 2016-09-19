---
title: "CWnd::SetCaretPos"
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
ms.assetid: f85c4213-fa54-49a3-8aaf-6208b96a9765
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetCaretPos
Sets the position of the caret.  
  
## Syntax  
  
```  
  
      static void PASCAL SetCaretPos(  
   POINT point   
);  
```  
  
#### Parameters  
 `point`  
 Specifies the new x and y coordinates (in client coordinates) of the caret.  
  
## Remarks  
 The `SetCaretPos` member function moves the caret only if it is owned by a window in the current task. `SetCaretPos` moves the caret whether or not the caret is hidden.  
  
 The caret is a shared resource. A window should not move the caret if it does not own the caret.  
  
## Example  
 [!CODE [NVC_MFCWindowing#115](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#115)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetCaretPos](../vs140/CWnd--GetCaretPos.md)   
 [SetCaretPos](http://msdn.microsoft.com/library/windows/desktop/ms648405)