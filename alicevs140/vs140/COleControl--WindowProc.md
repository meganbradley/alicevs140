---
title: "COleControl::WindowProc"
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
ms.assetid: 6483f351-d6a6-42b6-8482-a33d4fdb7fb5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::WindowProc
Provides a Windows procedure for a `COleControl` object.  
  
## Syntax  
  
```  
  
      virtual LRESULT WindowProc(  
   UINT message,  
   WPARAM wParam,  
   LPARAM lParam  
);  
```  
  
#### Parameters  
 `message`  
 Specifies the Windows message to be processed.  
  
 `wParam`  
 Provides additional information used in processing the message. The parameter value depends on the message.  
  
 `lParam`  
 Provides additional information used in processing the message. The parameter value depends on the message.  
  
## Return Value  
 The return value of the message dispatched.  
  
## Remarks  
 Call this function to dispatch specific messages through the control's message map.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)