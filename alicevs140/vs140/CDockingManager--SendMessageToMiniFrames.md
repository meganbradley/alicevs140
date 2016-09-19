---
title: "CDockingManager::SendMessageToMiniFrames"
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
ms.assetid: 89ad1197-b959-4ffe-8fb0-0f4a95f5fcbe
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::SendMessageToMiniFrames
Sends the specified message to all mini frames.  
  
## Syntax  
  
```  
BOOL SendMessageToMiniFrames(  
   UINT uMessage,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0  
);  
```  
  
#### Parameters  
 [in] `uMessage`  
 The message to be sent.  
  
 [in] `wParam`  
 Additional message dependent information.  
  
 [in] `lParam`  
 Additional message dependent information.  
  
## Return Value  
 `TRUE` always.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)