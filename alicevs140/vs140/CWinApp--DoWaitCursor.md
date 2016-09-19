---
title: "CWinApp::DoWaitCursor"
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
ms.assetid: 15697c83-a43d-4f22-a710-08e0d63e1b6b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::DoWaitCursor
This member function is called by the framework to implement [CWaitCursor](../vs140/CWaitCursor-Class.md), [CCmdTarget::BeginWaitCursor](../vs140/CCmdTarget--BeginWaitCursor.md), [CCmdTarget::EndWaitCursor](../vs140/CCmdTarget--EndWaitCursor.md), and [CCmdTarget::RestoreWaitCursor](../vs140/CCmdTarget--RestoreWaitCursor.md).  
  
## Syntax  
  
```  
  
      virtual void DoWaitCursor(  
   int nCode   
);  
```  
  
#### Parameters  
 `nCode`  
 If this parameter is 1, a wait cursor appears. If 0, the wait cursor is restored without incrementing the reference count. If –1, the wait cursor ends.  
  
## Remarks  
 The default implements an hourglass cursor. `DoWaitCursor` maintains a reference count. When positive, the hourglass cursor is displayed.  
  
 While you would not normally call `DoWaitCursor` directly, you could override this member function to change the wait cursor or to do additional processing while the wait cursor is displayed.  
  
 For an easier, more streamlined way to implement a wait cursor, use `CWaitCursor`.  
  
## Example  
 [!CODE [NVC_MFCWindowing#37](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#37)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdTarget::BeginWaitCursor](../vs140/CCmdTarget--BeginWaitCursor.md)   
 [CCmdTarget::EndWaitCursor](../vs140/CCmdTarget--EndWaitCursor.md)   
 [CCmdTarget::RestoreWaitCursor](../vs140/CCmdTarget--RestoreWaitCursor.md)   
 [CWaitCursor Class](../vs140/CWaitCursor-Class.md)