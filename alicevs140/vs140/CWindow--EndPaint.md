---
title: "CWindow::EndPaint"
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
ms.assetid: be3efc16-5854-48ff-89d6-11f63eaaa4dc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::EndPaint
Marks the end of painting.  
  
## Syntax  
  
```  
  
      void EndPaint(  
   LPPAINTSTRUCT lpPaint   
) throw();  
```  
  
## Remarks  
 See [EndPaint](http://msdn.microsoft.com/library/windows/desktop/dd162598) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#2](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#2)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::BeginPaint](../vs140/CWindow--BeginPaint.md)