---
title: "CWinApp::EnableTaskbarInteraction"
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
ms.assetid: f15b28c1-247c-4d69-acd8-9bfa96cd604f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::EnableTaskbarInteraction
Enables Taskbar interaction.  
  
## Syntax  
  
```  
BOOL EnableTaskbarInteraction(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 `bEnable`  
 Specifies whether interaction with Windows 7 taskbar should be enabled (`TRUE`), or disabled (`FALSE`).  
  
## Return Value  
 Returns `TRUE` if taskbar interaction can be enabled or disabled.  
  
## Remarks  
 This method must be called before creation of main window, otherwise it asserts and returns `FALSE`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)