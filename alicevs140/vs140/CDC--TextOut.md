---
title: "CDC::TextOut"
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
ms.assetid: 3c81bd37-a3d3-4550-bca6-7ebc3ac2d976
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::TextOut
Writes a character string at the specified location using the currently selected font.  
  
## Syntax  
  
```  
  
      virtual BOOL TextOut(  
   int x,  
   int y,  
   LPCTSTR lpszString,  
   int nCount   
);  
BOOL TextOut(  
   int x,  
   int y,  
   const CString& str   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the logical x-coordinate of the starting point of the text.  
  
 *y*  
 Specifies the logical y-coordinate of the starting point of the text.  
  
 `lpszString`  
 Points to the character string to be drawn.  
  
 `nCount`  
 Specifies the number of characters in the string.  
  
 `str`  
 A `CString` object that contains the characters to be drawn.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 Character origins are at the upper-left corner of the character cell. By default, the current position is not used or updated by the function.  
  
 If an application needs to update the current position when it calls `TextOut`, the application can call the `SetTextAlign` member function with `nFlags` set to **TA_UPDATECP**. When this flag is set, Windows ignores the *x* and *y* parameters on subsequent calls to `TextOut`, using the current position instead.  
  
## Example  
 See the example for [CDC::BeginPath](../vs140/CDC--BeginPath.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::ExtTextOut](../vs140/CDC--ExtTextOut.md)   
 [CDC::GetTextExtent](../vs140/CDC--GetTextExtent.md)   
 [CDC::SetTextAlign](../vs140/CDC--SetTextAlign.md)   
 [CDC::SetTextColor](../vs140/CDC--SetTextColor.md)   
 [CDC::TabbedTextOut](../vs140/CDC--TabbedTextOut.md)   
 [TextOut](http://msdn.microsoft.com/library/windows/desktop/dd145133)