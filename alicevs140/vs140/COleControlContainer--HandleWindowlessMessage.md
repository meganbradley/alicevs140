---
title: "COleControlContainer::HandleWindowlessMessage"
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
ms.assetid: b8573232-27dc-4477-a14e-d8c293e70082
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::HandleWindowlessMessage
Processes window messages for windowless controls.  
  
## Syntax  
  
```  
  
      virtual BOOL HandleWindowlessMessage(  
   UINT message,  
   WPARAM wParam,  
   LPARAM lParam,  
   LRESULT* plResult   
);  
```  
  
#### Parameters  
 `message`  
 The identifier for the window message, provided by Windows.  
  
 `wParam`  
 Parameter of the message; provided by Windows. Specifies additional message-specific information. The contents of this parameter depend on the value of the `message` parameter.  
  
 `lParam`  
 Parameter of the message; provided by Windows. Specifies additional message-specific information. The contents of this parameter depend on the value of the `message` parameter.  
  
 *plResult*  
 Windows result code. Specifies the result of the message processing and depends on the message sent.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 Override this function to customize the handling of windowless control messages.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)