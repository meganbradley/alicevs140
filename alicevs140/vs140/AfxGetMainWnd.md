---
title: "AfxGetMainWnd"
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
ms.topic: article
ms.assetid: 4977d098-13ea-4a47-863d-2f6e2fcd2a8f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetMainWnd
If your application is an OLE server, call this function to retrieve a pointer to the active main window of the application instead of directly referring to the [m_pMainWnd](../vs140/CWinThread--m_pMainWnd.md) member of the application object.  
  
## Syntax  
  
```  
  
CWnd* AFXAPI AfxGetMainWnd( );  
```  
  
## Return Value  
 If the server has an object that is in-place active inside a container, and this container is active, this function returns a pointer to the frame window object that contains the in-place active document.  
  
 If there is no object that is in-place active within a container, or your application is not an OLE server, this function simply returns the `m_pMainWnd` of your application object.  
  
 If `AfxGetMainWnd` is called from the application's primary thread, it returns the application's main window according to the above rules. If the function is called from a secondary thread in the application, the function returns the main window associated with the thread that made the call.  
  
## Remarks  
 If your application is not an OLE server, then calling this function is equivalent to directly referring to the `m_pMainWnd` member of your application object.  
  
## Example  
 [!CODE [NVC_MFCWindowing#129](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#129)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CWinThread::m_pMainWnd](../vs140/CWinThread--m_pMainWnd.md)