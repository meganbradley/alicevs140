---
title: "CDC::SetTextJustification"
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
ms.assetid: b4b1043d-1578-4d14-8e94-f4ebdfb4b39e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetTextJustification
Adds space to the break characters in a string.  
  
## Syntax  
  
```  
  
      int SetTextJustification(  
   int nBreakExtra,  
   int nBreakCount   
);  
```  
  
#### Parameters  
 `nBreakExtra`  
 Specifies the total extra space to be added to the line of text (in logical units). If the current mapping mode is not `MM_TEXT`, the value given by this parameter is converted to the current mapping mode and rounded to the nearest device unit.  
  
 *nBreakCount*  
 Specifies the number of break characters in the line.  
  
## Return Value  
 One if the function is successful; otherwise 0.  
  
## Remarks  
 An application can use the `GetTextMetrics` member functions to retrieve a font's break character.  
  
 After the `SetTextJustification` member function is called, a call to a text-output function (such as `TextOut`) distributes the specified extra space evenly among the specified number of break characters. The break character is usually the space character (ASCII 32), but may be defined by a font as some other character.  
  
 The member function `GetTextExtent` is typically used with `SetTextJustification`. `GetTextExtent` computes the width of a given line before alignment. An application can determine how much space to specify in the `nBreakExtra` parameter by subtracting the value returned by `GetTextExtent` from the width of the string after alignment.  
  
 The `SetTextJustification` function can be used to align a line that contains multiple runs in different fonts. In this case, the line must be created piecemeal by aligning and writing each run separately.  
  
 Because rounding errors can occur during alignment, the system keeps a running error term that defines the current error. When aligning a line that contains multiple runs, `GetTextExtent` automatically uses this error term when it computes the extent of the next run. This allows the text-output function to blend the error into the new run.  
  
 After each line has been aligned, this error term must be cleared to prevent it from being incorporated into the next line. The term can be cleared by calling `SetTextJustification` with `nBreakExtra` set to 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetMapMode](../vs140/CDC--GetMapMode.md)   
 [CDC::GetTextExtent](../vs140/CDC--GetTextExtent.md)   
 [CDC::GetTextMetrics](../vs140/CDC--GetTextMetrics.md)   
 [CDC::SetMapMode](../vs140/CDC--SetMapMode.md)   
 [CDC::TextOut](../vs140/CDC--TextOut.md)   
 [SetTextJustification](http://msdn.microsoft.com/library/windows/desktop/dd145094)