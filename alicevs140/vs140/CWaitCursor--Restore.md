---
title: "CWaitCursor::Restore"
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
ms.assetid: 2326c592-5ceb-47c4-9f3c-d3d97eed9cf8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWaitCursor::Restore
To restore the wait cursor, call this function after performing an operation, such as displaying a message box or dialog box, which might change the wait cursor to another cursor.  
  
## Syntax  
  
```  
  
void Restore( );  
  
```  
  
## Remarks  
 It is OK to call **Restore** even when the wait cursor is currently displayed.  
  
 If you need to restore the wait cursor while in a function other than the one in which the `CWaitCursor` object is declared, you can call [CCmdTarget::RestoreWaitCursor](../vs140/CCmdTarget--RestoreWaitCursor.md).  
  
## Example  
 [!CODE [NVC_MFCWindowing#64](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#64)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWaitCursor Class](../vs140/CWaitCursor-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCmdTarget::RestoreWaitCursor](../vs140/CCmdTarget--RestoreWaitCursor.md)