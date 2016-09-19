---
title: "CDocument::CanCloseFrame"
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
ms.assetid: 5b2730a7-5aae-47c0-afea-1dbdf17400e5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::CanCloseFrame
Called by the framework before a frame window displaying the document is closed.  
  
## Syntax  
  
```  
  
      virtual BOOL CanCloseFrame(  
   CFrameWnd* pFrame   
);  
```  
  
#### Parameters  
 `pFrame`  
 Points to the frame window of a view attached to the document.  
  
## Return Value  
 Nonzero if it is safe to close the frame window; otherwise 0.  
  
## Remarks  
 The default implementation checks if there are other frame windows displaying the document. If the specified frame window is the last one that displays the document, the function prompts the user to save the document if it has been modified. Override this function if you want to perform special processing when a frame window is closed. This is an advanced overridable.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::SaveModified](../vs140/CDocument--SaveModified.md)