---
title: "CCmdTarget::EndWaitCursor"
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
ms.assetid: 9e0b8fe7-33d6-4b85-9b32-a8c7fdc2f7ab
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::EndWaitCursor
Call this function after you have called the `BeginWaitCursor` member function to return from the hourglass cursor to the previous cursor.  
  
## Syntax  
  
```  
  
void EndWaitCursor( );  
```  
  
## Remarks  
 The framework also calls this member function after it has called the hourglass cursor.  
  
## Example  
 [!CODE [NVC_MFCDocView#43](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#43)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWaitCursor Class](../vs140/CWaitCursor-Class.md)   
 [CCmdTarget::BeginWaitCursor](../vs140/CCmdTarget--BeginWaitCursor.md)   
 [CCmdTarget::RestoreWaitCursor](../vs140/CCmdTarget--RestoreWaitCursor.md)   
 [CWinApp::DoWaitCursor](../vs140/CWinApp--DoWaitCursor.md)