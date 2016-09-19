---
title: "CWindowDC::CWindowDC"
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
ms.assetid: bb80deca-be6a-4f49-86a6-ef9b693a26f3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowDC::CWindowDC
Constructs a `CWindowDC` object that accesses the entire screen area (both client and nonclient) of the `CWnd` object pointed to by `pWnd`.  
  
## Syntax  
  
```  
  
      explicit CWindowDC(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 The window whose client area the device-context object will access.  
  
## Remarks  
 The constructor calls the Windows function [GetWindowDC](http://msdn.microsoft.com/library/windows/desktop/dd144947).  
  
 An exception (of type `CResourceException`) is thrown if the Windows `GetWindowDC` call fails. A device context may not be available if Windows has already allocated all of its available device contexts. Your application competes for the five common display contexts available at any given time under Windows.  
  
## Example  
 [!CODE [NVC_MFCDocView#188](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#188)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWindowDC Class](../vs140/CWindowDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC Class](../vs140/CDC-Class.md)   
 [CClientDC Class](../vs140/CClientDC-Class.md)   
 [CWnd Class](../vs140/CWnd-Class.md)