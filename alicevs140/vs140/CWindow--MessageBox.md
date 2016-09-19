---
title: "CWindow::MessageBox"
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
ms.assetid: e68e7bf1-9a71-4ae9-9b55-33e391f1f8da
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::MessageBox
Displays a message box.  
  
## Syntax  
  
```  
  
      int MessageBox(  
   LPCTSTR lpszText,  
   LPCTSTR lpszCaption = NULL,  
   UINT nType = MB_OK   
) throw();  
```  
  
## Remarks  
 See [MessageBox](http://msdn.microsoft.com/library/windows/desktop/ms645505) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#24](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#24)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)