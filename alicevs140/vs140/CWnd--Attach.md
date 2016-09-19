---
title: "CWnd::Attach"
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
ms.assetid: 942a5fe2-a845-49f5-854c-8b4176a07765
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::Attach
Attaches a Windows window to a `CWnd` object.  
  
## Syntax  
  
```  
  
      BOOL Attach(  
   HWND hWndNew   
);  
```  
  
#### Parameters  
 `hWndNew`  
 Specifies a handle to a Windows window.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 This example shows how to use Attach and Detach to map to the MDI client window.  
  
 [!CODE [NVC_MFCWindowing#67](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#67)]  
  
 [!CODE [NVC_MFCWindowing#68](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#68)]  
  
 [!CODE [NVC_MFCWindowing#69](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#69)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Detach](../vs140/CWnd--Detach.md)   
 [CWnd::m_hWnd](../vs140/CWnd--m_hWnd.md)   
 [CWnd::SubclassWindow](../vs140/CWnd--SubclassWindow.md)