---
title: "CCmdTarget::RestoreWaitCursor"
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
ms.assetid: ed4afeae-1b68-4123-a65c-5a8361340be0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::RestoreWaitCursor
Call this function to restore the appropriate hourglass cursor after the system cursor has changed (for example, after a message box has opened and then closed while in the middle of a lengthy operation).  
  
## Syntax  
  
```  
  
void RestoreWaitCursor( );  
  
```  
  
## Example  
 [!CODE [NVC_MFCDocView#43](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#43)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWaitCursor Class](../vs140/CWaitCursor-Class.md)   
 [CCmdTarget::EndWaitCursor](../vs140/CCmdTarget--EndWaitCursor.md)   
 [CCmdTarget::BeginWaitCursor](../vs140/CCmdTarget--BeginWaitCursor.md)   
 [CWinApp::DoWaitCursor](../vs140/CWinApp--DoWaitCursor.md)