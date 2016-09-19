---
title: "CMFCColorMenuButton::GetColorByCmdID"
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
ms.assetid: 65aa4fb6-0190-4e3b-a991-a749d7368811
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorMenuButton::GetColorByCmdID
Retrieves the color that corresponds to a specified command ID.  
  
## Syntax  
  
```  
static COLORREF GetColorByCmdID(  
   UINT uiCmdID   
);  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 A command ID.  
  
## Return Value  
 The color that corresponds to the specified command ID.  
  
## Remarks  
 Use this method when you have several color buttons in an application. When the user clicks a color button, the button sends its command ID in a `WM_COMMAND` message to its parent. The `GetColorByCmdID` method uses the command ID to retrieve the corresponding color.  
  
## Requirements  
 **Header:** afxcolormenubutton.h  
  
## See Also  
 [CMFCColorMenuButton Class](../vs140/CMFCColorMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)