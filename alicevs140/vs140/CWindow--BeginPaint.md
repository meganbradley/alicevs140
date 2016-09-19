---
title: "CWindow::BeginPaint"
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
ms.assetid: f7422ecb-deb6-4e8f-aad1-7b607d1752eb
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::BeginPaint
Prepares the window for painting.  
  
## Syntax  
  
```  
  
      HDC BeginPaint(  
   LPPAINTSTRUCT lpPaint   
) throw();  
```  
  
## Remarks  
 See [BeginPaint](http://msdn.microsoft.com/library/windows/desktop/dd183362) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#2](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#2)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::EndPaint](../vs140/CWindow--EndPaint.md)