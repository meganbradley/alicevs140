---
title: "CToolTipCtrl::GetDelayTime"
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
ms.assetid: c01465cd-6c86-4cb5-bb03-dfedd17de5e2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolTipCtrl::GetDelayTime
Retrieves the initial, pop-up, and reshow durations currently set for a tool tip control.  
  
## Syntax  
  
```  
  
      int GetDelayTime(  
   DWORD dwDuration   
) const;  
```  
  
#### Parameters  
 `dwDuration`  
 Flag that specifies which duration value will be retrieved. This parameter can be one of the following values:  
  
-   `TTDT_AUTOPOP` Retrieve the length of time the tool tip window remains visible if the pointer is stationary within a tool's bounding rectangle.  
  
-   `TTDT_INITIAL` Retrieve the length of time the pointer must remain stationary within a tool's bounding rectangle before the tool tip window appears.  
  
-   `TTDT_RESHOW` Retrieve the length of time it takes for subsequent tool tip windows to appear as the pointer moves from one tool to another.  
  
## Return Value  
 The specified delay time, in milliseconds  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TTM_GETDELAYTIME](http://msdn.microsoft.com/library/windows/desktop/bb760390), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolTipCtrl Class](../vs140/CToolTipCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolTipCtrl::SetDelayTime](../vs140/CToolTipCtrl--SetDelayTime.md)