---
title: "CCmdTarget::BeginWaitCursor"
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
ms.assetid: 48736a92-53cf-4b00-a581-7986e81208f7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::BeginWaitCursor
Call this function to display the cursor as an hourglass when you expect a command to take a noticeable time interval to execute.  
  
## Syntax  
  
```  
  
void BeginWaitCursor( );  
```  
  
## Remarks  
 The framework calls this function to show the user that it is busy, such as when a **CDocument** object loads or saves itself to a file.  
  
 The actions of `BeginWaitCursor` are not always effective outside of a single message handler as other actions, such as `OnSetCursor` handling, could change the cursor.  
  
 Call `EndWaitCursor` to restore the previous cursor.  
  
## Example  
 [!CODE [NVC_MFCDocView#43](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#43)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWaitCursor Class](../vs140/CWaitCursor-Class.md)   
 [CCmdTarget::EndWaitCursor](../vs140/CCmdTarget--EndWaitCursor.md)   
 [CCmdTarget::RestoreWaitCursor](../vs140/CCmdTarget--RestoreWaitCursor.md)   
 [CWinApp::DoWaitCursor](../vs140/CWinApp--DoWaitCursor.md)