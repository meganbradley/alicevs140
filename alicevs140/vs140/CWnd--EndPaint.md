---
title: "CWnd::EndPaint"
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
ms.assetid: 9e485268-c9b9-4772-8960-58fe5f502057
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::EndPaint
Marks the end of painting in the given window.  
  
## Syntax  
  
```  
  
      void EndPaint(  
   LPPAINTSTRUCT lpPaint   
);  
```  
  
#### Parameters  
 `lpPaint`  
 Points to a [PAINTSTRUCT](../vs140/PAINTSTRUCT-Structure.md) structure that contains the painting information retrieved by the [BeginPaint](../vs140/CWnd--BeginPaint.md) member function.  
  
## Remarks  
 The `EndPaint` member function is required for each call to the `BeginPaint` member function, but only after painting is complete.  
  
 If the caret was hidden by the `BeginPaint` member function, `EndPaint` restores the caret to the screen.  
  
## Example  
 See the example for [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md)   
 [EndPaint](http://msdn.microsoft.com/library/windows/desktop/dd162598)   
 [CPaintDC Class](../vs140/CPaintDC-Class.md)