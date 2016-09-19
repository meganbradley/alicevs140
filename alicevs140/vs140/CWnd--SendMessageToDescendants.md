---
title: "CWnd::SendMessageToDescendants"
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
ms.assetid: e1b1a63f-93ed-4fd0-84cf-245b716cb1d7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SendMessageToDescendants
Call this member function to send the specified Windows message to all descendant windows.  
  
## Syntax  
  
```  
  
      void SendMessageToDescendants(  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0,  
   BOOL bDeep = TRUE,  
   BOOL bOnlyPerm = FALSE   
);  
```  
  
#### Parameters  
 `message`  
 Specifies the message to be sent.  
  
 `wParam`  
 Specifies additional message-dependent information.  
  
 `lParam`  
 Specifies additional message-dependent information.  
  
 `bDeep`  
 Specifies the level to which to search. If **TRUE**, recursively search all children; if **FALSE**, search only immediate children.  
  
 `bOnlyPerm`  
 Specifies whether the message will be received by temporary windows. If **TRUE**, temporary windows can receive the message; if **FALSE**, only permanent windows receive the message. For more information on temporary windows see [Technical Note 3](../vs140/TN003--Mapping-of-Windows-Handles-to-Objects.md).  
  
## Remarks  
 If `bDeep` is **FALSE**, the message is sent just to the immediate children of the window; otherwise the message is sent to all descendant windows.  
  
 If `bDeep` and `bOnlyPerm` are **TRUE**, the search continues below temporary windows. In this case, only permanent windows encountered during the search receive the message. If `bDeep` is **FALSE**, the message is sent only to the immediate children of the window.  
  
## Example  
 [!CODE [NVC_MFCWindowing#114](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#114)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SendMessage](../vs140/CWnd--SendMessage.md)   
 [CWnd::FromHandlePermanent](../vs140/CWnd--FromHandlePermanent.md)   
 [CWnd::FromHandle](../vs140/CWnd--FromHandle.md)