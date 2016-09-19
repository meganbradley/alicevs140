---
title: "CWindow::EnableWindow"
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
ms.assetid: 92746872-74df-46a7-9187-42aff98bb382
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::EnableWindow
Enables or disables input.  
  
## Syntax  
  
```  
  
      BOOL EnableWindow(  
   BOOL bEnable = TRUE   
) throw();  
```  
  
## Remarks  
 See [EnableWindow](http://msdn.microsoft.com/library/windows/desktop/ms646291) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATL_Windowing#7](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#7)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::IsWindowEnabled](../vs140/CWindow--IsWindowEnabled.md)