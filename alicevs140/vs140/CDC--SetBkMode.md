---
title: "CDC::SetBkMode"
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
ms.assetid: 671fedb7-6648-4a69-a624-34a57be86112
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetBkMode
Sets the background mode.  
  
## Syntax  
  
```  
  
      int SetBkMode(  
   int nBkMode   
);  
```  
  
#### Parameters  
 *nBkMode*  
 Specifies the mode to be set. This parameter can be either of the following values:  
  
-   **OPAQUE** Background is filled with the current background color before the text, hatched brush, or pen is drawn. This is the default background mode.  
  
-   **TRANSPARENT** Background is not changed before drawing.  
  
## Return Value  
 The previous background mode.  
  
## Remarks  
 The background mode defines whether the system removes existing background colors on the drawing surface before drawing text, hatched brushes, or any pen style that is not a solid line.  
  
## Example  
 See the example for [CWnd::OnCtlColor](../vs140/CWnd--OnCtlColor.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetBkColor](../vs140/CDC--GetBkColor.md)   
 [CDC::GetBkMode](../vs140/CDC--GetBkMode.md)   
 [CDC::SetBkColor](../vs140/CDC--SetBkColor.md)   
 [SetBkMode](http://msdn.microsoft.com/library/windows/desktop/dd162965)