---
title: "CMFCTasksPane::SetCaption"
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
ms.assetid: 9aa0dc24-c32d-4b33-9b4d-d42ce0b2fee9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetCaption
Sets the caption name of a task pane.  
  
## Syntax  
  
```  
void SetCaption(  
    LPCTSTR lpszName  
);  
```  
  
#### Parameters  
 [in] `lpszName`  
 Specifies the caption name.  
  
## Remarks  
 If a task pane has multiple pages, the default page has the caption that was set by using this function.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)